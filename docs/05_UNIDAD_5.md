# Unidad 5 — Redes, persistencia y estado

[Volver al índice](00_INDICE.md)

**Estado: Documentación completa respecto del material disponible.** Se integraron los dos PDF disponibles. **Sin material audiovisual, confirmado por el usuario.** No quedan búsquedas ni integraciones de videos pendientes para esta unidad.

## Fuentes y alcance

| Referencia | Fuente original | Páginas |
| --- | --- | --- |
| **Redes** | [U05.T01 - Redes.pdf](../fuentes/pdf/U05.T01%20-%20Redes.pdf) | 23 |
| **Persistencia** | [U05.T02 - Persistencia y estado.pdf](../fuentes/pdf/U05.T02%20-%20Persistencia%20y%20estado.pdf) | 28 |

El programa, p. 3, incluye Fetch, Axios, manejo de errores, AsyncStorage, SQLite y cambios de conectividad. El PDF de persistencia propone `expo-sqlite/kv-store` en lugar de AsyncStorage y se documenta esa diferencia. Los números de página son los del visor, incluida la portada. Los ejemplos se registran para estudiar, sin ejecutar requests, modificar bases ni instalar dependencias. El PDF Redes se cuenta una sola vez.

## 1. La red es una condición variable

En un teléfono, la conexión puede interrumpirse, cambiar de Wi-Fi a datos o mantener un enlace con una red sin acceso a internet. Por eso carga y error forman parte del diseño, no son situaciones ajenas a una pantalla terminada. La fuente contrapone una pantalla vacía con una que explica el problema y ofrece reintentar. **Fuente: Redes, pp. 4 y 7.**

Un request debe contemplar al menos **cargando**, **error con salida** y **datos**. Si el usuario cambia de búsqueda o abandona la pantalla, también debe considerarse la cancelación para no aplicar respuestas que dejaron de ser relevantes. **Fuente: Redes, pp. 7–8.**

## 2. Fetch y errores HTTP

`fetch` está disponible como API global de React Native y trabaja con promesas. La respuesta y la lectura del cuerpo son pasos diferentes. Un `404` o un `500` no equivale a que la promesa de `fetch` se rechace por ese estado; debe inspeccionarse la respuesta. **Fuente: Redes, pp. 5–6.**

```ts
try {
  const r = await fetch(url);
  if (!r.ok) {
    throw new Error(`El servidor respondió ${r.status}`);
  }
  mostrar(await r.json());
} catch (e) {
  mostrarError(e);
}
```

**Fuente: Redes, p. 6.** El `catch` también puede recibir fallos de red y lectura; no conviene confundirlos todos con un mismo mensaje de negocio.

### Cancelación

`AbortController` proporciona una señal al request y permite cancelarlo al limpiar un efecto. El ejemplo pasa `{ signal: control.signal }`, ejecuta `control.abort()` en el retorno y distingue `AbortError` de un error que deba mostrarse. **Fuente: Redes, p. 8.**

Esto es importante en búsquedas sucesivas: sin coordinar solicitudes, una respuesta lenta de una búsqueda anterior puede reemplazar el resultado más reciente. **Fuente: Redes, p. 8.**

**Aclaración editorial:** los `catch` de las diapositivas acceden directamente a propiedades de `e`. Son fragmentos simplificados; un proyecto TypeScript con errores de tipo `unknown` necesita identificar el error antes de acceder a sus propiedades. No se presupone esa configuración en los ejemplos.

## 3. Axios: centralizar comunicación

La clase presenta Axios para resolver tareas repetidas: JSON en `response.data`, rechazo ante estados HTTP de error, timeout e interceptores. También acepta la señal de `AbortController`. **Fuente: Redes, p. 10.**

```ts
import axios from 'axios';

export const api = axios.create({
  baseURL: process.env.EXPO_PUBLIC_API_URL,
  timeout: 10_000,
  headers: { 'Content-Type': 'application/json' },
});

const { data } = await api.get('/productos');
await api.post('/productos', { nombre, precio });
```

**Fuente: Redes, p. 11.** Una única instancia evita repetir la URL y la configuración en cada pantalla. La variable del ejemplo es la dirección pública de la API, no un secreto.

### Interceptores y diagnóstico

Un interceptor de request obtiene el token y agrega `Authorization: Bearer ...`. Uno de respuesta detecta un `401`, coordina el cierre de sesión y vuelve a rechazar el error para que no desaparezca del flujo. **Fuente: Redes, p. 12.**

El material distingue tres casos:

| Forma del error | Interpretación de la clase |
| --- | --- |
| Existe `response` | El servidor respondió; hay estado y posiblemente datos del error. |
| Existe `request`, sin respuesta | Se inició la solicitud, pero no se obtuvo respuesta. |
| No existen los anteriores | El pedido no se preparó correctamente. |

Esto permite diferenciar «el producto no existe» de «no pudimos conectarnos». **Fuente: Redes, p. 13.**

Fetch puede alcanzar para pocas llamadas sin autenticación ni dependencias adicionales. Axios resulta útil con varios endpoints, sesión y comportamiento compartido. Ninguno decide por sí solo cuánto tiempo sirve un dato ni cómo compartir su caché. **Fuente: Redes, p. 14.**

## 4. Estado del cliente y estado del servidor

| Estado del cliente | Estado del servidor |
| --- | --- |
| Tema, formulario, modal, selección local. | Productos, pedidos o perfil obtenidos de una API. |
| La aplicación controla su valor. | La aplicación mantiene una copia de un dato externo. |
| Puede manejarse con estado React o un store. | Puede envejecer, fallar y requerir resincronización. |

**Fuente: Redes, p. 16.**

El objetivo de TanStack Query es administrar esa copia: caché compartida, deduplicación, reintentos, invalidación y refresco. No reemplaza Fetch o Axios, que continúan transportando los datos. Evita mantener copias independientes de una misma respuesta en varias pantallas. **Fuente: Redes, pp. 16–17.**

### Lectura con `useQuery`

```tsx
const { data, isPending, error } = useQuery({
  queryKey: ['productos'],
  queryFn: () => api.get('/productos').then(r => r.data),
});
```

**Fuente: Redes, p. 17.**

- **`queryKey`:** identifica el dato; debe incluir lo que cambia el resultado, como categoría o página.
- **`queryFn`:** obtiene el dato o lanza un error.
- **`staleTime`:** expresa durante cuánto tiempo se considera fresca la copia.
- **`gcTime`:** expresa cuánto permanece una consulta inactiva antes de su eliminación de memoria.
- **`retry`:** configura reintentos.

El ejemplo utiliza `staleTime: 60_000` y diferencia envejecimiento de eliminación: un dato viejo todavía puede mostrarse mientras se comprueba de nuevo. **Fuente: Redes, p. 18.**

### Escritura con `useMutation`

Una mutación se dispara por una acción, no solo por montar el componente. Crear un registro es un efecto que no debe duplicarse por reintentos indiscriminados. La fuente vincula escritura e invalidación:

```tsx
const crear = useMutation({
  mutationFn: (nuevo) => api.post('/productos', nuevo).then(r => r.data),
  onSuccess: () => queryClient.invalidateQueries({ queryKey: ['productos'] }),
  onError: (e) => mostrarError(e),
});

<Button title="Guardar" onPress={() => crear.mutate({ nombre, precio })} />
```

**Fuente: Redes, pp. 19–20.** `queryClient` se obtiene con `useQueryClient`. Invalidar comunica que la lectura debe revisarse después del cambio.

**Aclaración editorial:** la p. 19 simplifica mutación como escritura «no cacheada» y retorno de confirmación. Para estos apuntes se conserva el criterio de diseño —no tratarla como una consulta compartida—, sin suponer que su resultado carezca de datos o de estado propio.

### Actualización optimista y proveedores

La actualización optimista modifica la pantalla antes de la respuesta. El ejemplo marca una tarea como hecha: cancela consultas relacionadas, guarda la copia previa y cambia la caché. Si falla, restaura la copia; al terminar, invalida para resincronizar. Sin rollback, la interfaz puede mostrar como confirmado algo que nunca se guardó. **Fuente: Redes, p. 21.**

La app se envuelve en `QueryClientProvider`. Para el foco móvil, la presentación conecta `AppState` con `focusManager.setFocused(estado === 'active')`. Así se informa a la librería cuándo la app vuelve al primer plano. **Fuente: Redes, p. 22.**

## 5. Dónde guardar cada dato

Persistir significa conservar datos más allá del estado en memoria. La elección depende del tipo, tamaño, consultas, sensibilidad y necesidad de trabajo sin red. **Fuente: Persistencia, pp. 4 y 11.**

| Dato | Solución del material |
| --- | --- |
| Preferencias y valores pequeños | `expo-sqlite/kv-store`. |
| Registros relacionados y consultas | `expo-sqlite`. |
| Tokens y credenciales | `expo-secure-store`, desarrollado en Unidad 6. |
| Fotos, PDF y adjuntos | Archivos, desarrollados en Unidad 4. |
| Copia de respuestas de una API | Caché de estado del servidor con TanStack Query. |

**Fuente: Persistencia, p. 4.** Caché, estado global y almacenamiento duradero resuelven problemas diferentes.

### Clave-valor: de AsyncStorage a `kv-store`

El programa menciona AsyncStorage. La presentación muestra su API para reconocerla y adopta `expo-sqlite/kv-store`, manteniendo operaciones equivalentes e incorporando variantes síncronas. Es una decisión del material de la cursada, no una declaración de que AsyncStorage haya dejado de existir. **Fuentes: Programa, p. 3; Persistencia, p. 6.**

```ts
import Storage from 'expo-sqlite/kv-store';

await Storage.setItem('tema', 'oscuro');
const tema = await Storage.getItem('tema');
await Storage.setItem('usuario', JSON.stringify({ id: 7, nombre: 'Ana' }));
const crudo = await Storage.getItem('usuario');
const usuario = crudo ? JSON.parse(crudo) : null;
await Storage.removeItem('usuario');
```

**Fuente: Persistencia, pp. 6 y 8.** Se guardan cadenas; objetos necesitan serialización y la ausencia devuelve `null`. La fuente recomienda encapsular lectura y escritura con tratamiento de errores de JSON.

Para preferencias pequeñas de inicio muestra `useState(() => Storage.getItemSync('tema') ?? 'claro')`, evitando un primer render con otro tema. No propone sincronía para operaciones grandes. Aquí no van tokens, grandes colecciones consultables ni imágenes base64. **Fuente: Persistencia, pp. 7–9.**

## 6. SQLite: relaciones, migraciones y transacciones

SQLite resulta apropiado cuando hay muchos registros, relaciones, filtros, ordenamiento o trabajo sin conexión. No aporta una ventaja clara para cuatro preferencias leídas completas. La aplicación puede reutilizar conocimientos de SQL, índices, `WHERE` y `JOIN`. **Fuente: Persistencia, p. 11.**

### Proveedor y operaciones

```tsx
<SQLiteProvider databaseName="app.db" onInit={migrar}>
  <Slot />
</SQLiteProvider>
```

Los descendientes acceden con `useSQLiteContext()`. La inicialización prepara la base antes de las consultas de las pantallas. **Fuente: Persistencia, p. 12.**

| Método | Uso |
| --- | --- |
| `execAsync` | Sentencias de esquema; no introducir datos de usuario concatenados. |
| `runAsync` | Insertar, modificar o borrar; informa identificador y cantidad afectada. |
| `getFirstAsync` | Una fila o `null`. |
| `getAllAsync` | Arreglo de filas. |

**Fuente: Persistencia, p. 13.** La fuente muestra variantes síncronas, pero prefiere asincronía para no bloquear JS en consultas grandes.

### Parámetros

```ts
await db.getAllAsync(
  'SELECT * FROM usuarios WHERE nombre = ?',
  entrada,
);
```

Separar consulta y valores evita que el texto del usuario se interprete como instrucciones SQL. No se concatena `entrada` dentro de una sentencia. **Fuente: Persistencia, p. 14.**

**Aclaración editorial:** la misma p. 14 incluye un `UPDATE` que mezcla un arreglo posicional y un objeto nombrado en una llamada. No se reproduce como receta validada; el ejemplo anterior conserva el caso claro de parámetros que sí desarrolla la diapositiva.

### Migraciones

La base puede sobrevivir a una actualización. Crear tablas solo para instalaciones nuevas no resuelve cómo modificar el esquema que ya tienen usuarios anteriores. El ejemplo lee `PRAGMA user_version`, compara contra una versión esperada, crea la tabla `tareas` cuando la versión es cero y actualiza el número. También muestra `PRAGMA journal_mode = 'wal'`. **Fuente: Persistencia, p. 15.**

El concepto importante es encadenar cambios de esquema según la versión existente. Reinstalar durante desarrollo puede ocultar un error de migración que aparecerá al actualizar. **Fuente: Persistencia, p. 15.**

### Transacciones

`withTransactionAsync` agrupa en el ejemplo un pedido y sus ítems. La intención es confirmar el conjunto o no dejarlo a medias si una operación falla. Evita un pedido incompleto y reduce el costo de escrituras separadas. **Fuente: Persistencia, p. 16.**

## 7. Estado global

Se comienza por preguntar quién necesita el dato. Si lo utiliza una pantalla con sus hijos, puede bastar `useState`. Si muchas pantallas leen un dato de baja frecuencia, Context puede ser suficiente. Si la fuente de verdad es el servidor, ya existe la caché compartida de Query. Un estado de cliente frecuente entre pantallas independientes puede justificar Zustand. **Fuente: Persistencia, pp. 18–19.**

### Context y proveedor

El ejemplo de carrito crea un contexto con `items`, `agregar` y `quitar`; un proveedor mantiene el estado y envuelve `Slot`. El hook `useCarrito()` lo lee y lanza un error descriptivo si falta el proveedor. **Fuente: Persistencia, pp. 20–21.**

El costo señalado es que los consumidores de ese contexto reciben el valor completo: si cambia el arreglo, también pueden renderizarse quienes solo usan una de sus funciones. **Aclaración editorial:** la p. 18 dice «todo el árbol», mientras la p. 21 precisa los componentes consumidores. Se conserva esta última explicación, sin atribuir necesariamente el mismo renderizado a todo descendiente. **Fuente: Persistencia, pp. 18 y 21.**

### Zustand y selectores

El store se crea con `create`, conserva estado y funciones en un objeto y se consume como hook. El ejemplo agrega y quita ítems y calcula el total con `get().items.reduce(...)`. **Fuente: Persistencia, p. 22.**

```ts
const cantidad = useCarrito(s => s.items.length);
const agregar = useCarrito(s => s.agregar);
```

Los selectores limitan a qué parte del store se suscribe un componente. Consumir todo con `useCarrito()` hace que cualquier cambio del store lo afecte. **Fuente: Persistencia, p. 23.**

Para conservar el carrito entre cierres, el ejemplo incorpora `persist`, `createJSONStorage(() => Storage)` y `partialize: s => ({ items: s.items })`. Así se persisten datos en `kv-store` sin intentar serializar funciones. **Fuente: Persistencia, p. 24.**

## 8. Conectividad y utilidad sin conexión

`useNetworkState()` de `expo-network` distingue conectividad con una red de alcance real de internet. Un portal cautivo puede dejar `isConnected` verdadero sin que los datos lleguen al servidor. El ejemplo muestra una barra cuando `isInternetReachable === false` y otra si se usan datos móviles. **Fuente: Persistencia, p. 26.**

La propuesta de diseño es diferente para lectura y escritura:

- **Lectura:** mostrar lo último disponible, informar que puede estar viejo y ofrecer un reintento.
- **Escritura:** guardar localmente, identificar lo pendiente y sincronizar al recuperar conexión.

Una tabla SQLite de pendientes permite representar ese trabajo. La fuente no implementa el algoritmo completo de sincronización, resolución de conflictos o duplicados; no se lo presupone resuelto por detectar que volvió la red. La práctica es probar en modo avión y evitar un spinner indefinido. **Fuente: Persistencia, p. 27.**

## Cierre y cobertura

- Ambos PDF quedaron integrados; Redes figura una sola vez.
- Se conserva la diferencia entre AsyncStorage del programa y `kv-store` del material.
- La sincronización offline se presenta al nivel conceptual de la fuente, sin inventar backend ni protocolo.
- **Sin material audiovisual, confirmado por el usuario.** No quedan tareas de búsqueda o integración de videos.

La Unidad 5 queda como **Documentación completa respecto del material disponible**, conservando los contenidos y referencias de ambos PDF y los límites conceptuales de sus ejemplos.
