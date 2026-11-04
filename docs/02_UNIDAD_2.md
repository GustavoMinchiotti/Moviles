# Unidad 2 — TypeScript, React, ciclo de vida, testing y rendimiento

[Volver al índice](00_INDICE.md)

**Estado: Documentación completa respecto del material disponible. Audiovisuales: 2 de 2 incorporados.** Se conservan los tres PDF y los aportes del **20/08/2026**, y se integran por tema los recibidos de **«GRABACIÓN CLASE UNIDAD II - 27/08/2026»**, segundo y último video confirmado por el usuario. Los límites de las transcripciones y de cobertura se registran sin bloquear el cierre. No quedan búsquedas pendientes de más grabaciones por anuncios hechos durante las clases.

## Fuentes y alcance

| Referencia | Fuente original | Alcance |
| --- | --- | --- |
| **React** | [U02 — TypeScript, React y ciclo de vida · Desarrollo para Móviles.pdf](../fuentes/pdf/U02%20%E2%80%94%20TypeScript%2C%20React%20y%20ciclo%20de%20vida%20%C2%B7%20Desarrollo%20para%20Mo%CC%81viles.pdf) | 43 |
| **Testing** | [U02 — Testing.pdf](../fuentes/pdf/U02%20%E2%80%94%20Testing.pdf) | 24 |
| **Depuración** | [U02 — Depuración y rendimiento.pdf](../fuentes/pdf/U02%20%E2%80%94%20Depuracio%CC%81n%20y%20rendimiento.pdf) | 26 |
| **Clase 20/08/2026** | [GRABACIÓN CLASE UNIDAD II - 20/08/2026](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=55401) | Primer video de los dos confirmados. El usuario informa que la transcripción automática llega a 1:47:56; los aportes detallados recibidos incluyen marcas hasta 1:39:45. |
| **Clase 27/08/2026** | «GRABACIÓN CLASE UNIDAD II - 27/08/2026». Transcripción automática identificada por el usuario; enlace no proporcionado. | Segundo y último video confirmado. El texto recibido, según lo informado, termina a los 59:58 en medio de una intervención; esto no demuestra que la grabación termine allí. |

El programa, p. 3, incluye repaso de TypeScript/React, React Native con Expo, flujo de trabajo, DOM frente a componentes nativos, inicio de proyecto y ciclo de vida. Se integran también testing y depuración porque los PDF los identifican como parte de la Unidad 2. Los números de página corresponden al visor, incluida la portada. Los ejemplos son fragmentos de las fuentes; sus dependencias y funciones auxiliares no se consideran un proyecto completo. Las versiones y herramientas mencionadas conservan el contexto de las presentaciones, sin verificación externa.

**Límite de la clase del 20/08/2026:** el adjunto contiene un listado de aportes y marcas de tiempo, no el cuerpo literal íntegro de los subtítulos. El enlace del campus no pudo consultarse desde la herramienta disponible. Se integra lo respaldado por ese listado sin atribuirle una revisión directa del video ni reconstruir lo ocurrido en intervalos no detallados, incluido el tramo final hasta 1:47:56. Los ejemplos nuevos de código se identifican expresamente como reconstrucciones didácticas y no como copias de pantalla.

**Límite de la clase del 27/08/2026:** la incorporación utiliza los aportes y las marcas incluidos en el pedido, no una revisión directa del video ni un cuerpo literal completo de transcripción. Se conserva el corte informado del texto a los **59:58**, en medio de una intervención, sin afirmar que ese sea el final del video. No se reutiliza el enlace del 20/08 ni se inventa uno nuevo. Anuncios, propuestas y ejemplos se distinguen de entregas efectivas y condiciones definitivas; los cupos de EAS o condiciones comerciales mencionados no se consideran datos actuales verificados.

## Preparación, proyecto Expo y ejemplo de requisitos

### Condiciones de trabajo anunciadas el 20/08/2026

El docente aclara que **el emulador no es obligatorio para programar**, que se puede comenzar con **Expo Go** y que se mostrarán alternativas para código nativo, emulador y teléfono. Tampoco se exige levantar ambos entornos, Android e iOS. Son condiciones de cursada expresadas en esa fecha, distintas de los requisitos técnicos que impone cada alternativa cuando se elige utilizarla. **Fuente: Clase 20/08/2026, 00:00–04:08, según los aportes recibidos.**

### «Mi ciudad»: de la necesidad del cliente a las funciones

Se presenta como ejemplo de **PRD**, documento de requisitos de producto, una guía turística llamada **«Mi ciudad»**. El recorrido contempla lugares cercanos, mapas, favoritos, QR, multimedia, notificaciones, almacenamiento y sincronización. **Fuente: Clase 20/08/2026, 04:18–17:30, según los aportes recibidos.**

**Organización editorial para estudiar el ejemplo:** primero se identifica el problema del cliente, después se expresan requisitos y se toman decisiones de diseño, y finalmente se los vincula con funcionalidades concretas. La lista de capacidades no sustituye explicar para quién sirve la guía y cómo cada decisión responde a una necesidad. El listado recibido no permite atribuir al docente un detalle adicional de cada requisito o afirmar que todo estuviera implementado.

Es un **ejemplo de PRD presentado**, no una consigna definitiva para todos los grupos. En ese fragmento las otras propuestas y APIs estaban anunciadas, no entregadas. **Fuente: Clase 20/08/2026, 04:18–17:30, según los aportes recibidos.**

#### Ampliación de la lectura del PRD el 27/08/2026

La segunda clase profundiza la lectura de la guía turística: relaciona contexto del problema, requisitos, datos y alcance antes de decidir cómo construir la aplicación. El docente lo presenta como **caso didáctico elaborado con IA**; no se registran sus personajes, cifras o sucesos como hechos reales. **Fuente: Clase 27/08/2026, 26:46–45:30, según los aportes recibidos.**

| Área del ejemplo | Capacidades y decisiones identificadas |
| --- | --- |
| Exploración de lugares | Categorías, búsqueda, detalle y horarios. |
| Ubicación | Mapa, cercanía y apertura de una aplicación de mapas. |
| Agenda | Eventos de interés para quien consulta la guía. |
| Registro de visitas | QR, fotografías y notas. |
| Funciones personales | Favoritos y cuenta; diferencia entre consulta pública y operaciones que requieren autenticación. |
| Contenido | Audioguías y recursos relacionados con los lugares. |
| Condiciones de uso | Manejar falta de conexión, permisos denegados y tamaño de letra configurado por el usuario. |

**Fuente: Clase 27/08/2026, 26:46–45:30.** La tabla organiza los aportes recibidos; no reproduce un contrato completo de datos ni asigna por inferencia autenticación a cada funcionalidad.

Las pantallas y la navegación pueden ajustarse si se justifican las decisiones. La libertad de diseño no elimina los requisitos del PRD elegido. En este ejemplo, **reservas y pagos quedan fuera del MVP**, la versión mínima del producto. Una posible reducción, como registrar visitas solo por QR, se conserva como propuesta, no como cambio definitivo de consigna. La transcripción y estos apuntes **no sustituyen al PRD completo**. **Fuente: Clase 27/08/2026, 26:46–45:30.**

#### Desarrollo por etapas, mocks y servicios

Mientras se prepara la API, la clase propone comenzar con datos simulados, definir interfaces para entidades y respuestas y hacer que las pantallas consuman **servicios**. Los mocks se encapsulan en esos servicios para reemplazarlos después por llamadas a la API sin trasladar esa sustitución a cada pantalla. **Fuente: Clase 27/08/2026, 42:00–43:36.**

El aporte es una separación de responsabilidades, no un contrato ya implementado: las pantallas utilizan las operaciones del servicio y este resuelve de dónde obtiene los datos. No se reconstruyen firmas de funciones, respuestas completas ni código que solo hubiera estado visible en pantalla.

Como secuencia de avance se propone trabajar **pantallas y navegación → formularios → funcionalidades → conexión a la API**. Las etapas ayudan a distinguir una pantalla que usa mocks de una integración efectiva con un servidor; no equivalen a declarar terminado el proyecto al completar las primeras. **Fuente: Clase 27/08/2026, 52:02–58:09.**

#### Temáticas anunciadas

Se anuncian cinco propuestas: **guía turística, reporte ciudadano, transporte público, directorio de comercios y reservas deportivas**. Cada grupo elige una y puede consultar otras ideas. De las cuatro que no se desarrollan aquí no se inventan requisitos. **Fuente: Clase 27/08/2026, 45:33–46:23.**

### Orientaciones del integrador anunciadas el 27/08/2026

Estas indicaciones amplían los anuncios del 20/08 y se conservan con su fecha. La aplicación se plantea con **React Native y Expo según el PRD elegido**: sus pantallas y funciones se determinan a partir de ese documento. Se incluye registro, login, mantenimiento de sesión y acceso rápido mediante mecanismos de seguridad del dispositivo; consumo de API, persistencia y capacidades del dispositivo dependen de los requisitos del proyecto. **Fuente: Clase 27/08/2026, 06:03–16:44.**

El alcance planteado para login utiliza **usuario y contraseña**. Los comentarios sobre Google o servicios pagos no se convierten en restricciones técnicas universales. El alcance de las notificaciones locales y push se mantiene como aspecto tentativo de la discusión, no como obligación uniforme confirmada para todos los proyectos. **Fuente: Clase 27/08/2026, 06:03–16:44 y 16:46–25:50, según los aportes recibidos.**

#### Entrega y preparación del build

- **Entrega grupal:** código mediante repositorio o ZIP **sin `node_modules`**, incluyendo la configuración, y enlace del **build de preview**.
- **Fecha:** se informaría en el campus; no se fija una fecha a partir de ejemplos o estimaciones orales.
- **Preparación:** probar el build con anticipación para no descubrir problemas de compilación o instalación al entregar.

**Fuente: Clase 27/08/2026, 06:03–16:44.** Se registran las indicaciones anunciadas, sin verificar cupos comerciales ni afirmar que el proyecto o su build ya se hayan entregado. El proceso de construcción se desarrolla en Unidad 7.

#### Defensa y evaluación

Se anuncia una **defensa grupal en vivo de 15 a 20 minutos**, con explicación del aporte de cada integrante y preguntas sobre su código. La entrega es grupal, pero la **calificación es individual**. El uso de IA durante el desarrollo está permitido con comprensión y capacidad para explicar lo implementado. Según lo anunciado, aprobar el parcial habilita la presentación del integrador, y **sin defensa no se considera aprobado**. **Fuente: Clase 27/08/2026, 09:17–10:58 y 16:46–25:50.**

Entre los ejemplos de preguntas aparecen justificar **`FlatList` frente a `ScrollView`**, explicar optimizaciones y fundamentar decisiones de implementación. Son orientaciones para preparar la explicación, no un cuestionario cerrado ni una garantía de aprobación. El comentario informal «si funciona ya es un seis» no se interpreta como una nota asegurada: la evaluación se condiciona también a la defensa. No se fijan fechas definitivas desde estimaciones de la conversación. **Fuente: Clase 27/08/2026, 16:46–25:50.**

### Creación y plantillas

La demostración recorre la creación de un proyecto, la elección de plantilla y la comparación de dos plantillas. Permite observar que la estructura inicial y los componentes de ejemplo dependen de esa elección. **Fuente: Clase 20/08/2026, 18:11–48:22, según los aportes recibidos.**

**Límite de reconstrucción:** el adjunto no identifica de forma inequívoca los nombres, las opciones exactas ni la correspondencia de cada diferencia con una de las dos plantillas. Por eso no se fija aquí un árbol por plantilla ni se reconstruyen flags o comandos a partir de subtítulos ambiguos. El recorrido siguiente describe las piezas identificadas, sin asumir que todas estén presentes en cualquier plantilla.

| Archivo o área | Función para leer el proyecto |
| --- | --- |
| `package.json` | Dependencias, scripts y metadatos del proyecto JavaScript. |
| `.gitignore` | Patrones de archivos que no se incorporan al seguimiento ordinario de Git. |
| `app.json` | Configuración de la aplicación Expo. |
| `assets` | Recursos del ejemplo, como imágenes o fuentes; no es su única ubicación posible. |
| Pantallas y rutas | Entradas de navegación organizadas por archivos en el proyecto mostrado. |
| Componentes | Interfaz reutilizable entre pantallas. |
| Hooks | Lógica reutilizable que utiliza las capacidades de React. |
| Constantes | Valores compartidos, como colores, para evitar repetir definiciones. |

**Fuente: Clase 20/08/2026, 18:11–48:22, según los aportes recibidos.** Se utiliza la tabla como organización conceptual, no como transcripción literal de un árbol de directorios.

El recorrido introduce layout raíz, grupos de rutas, tabs y modal; también presenta librerías para íconos, fuentes, vibración, imágenes, enlaces y navegador, y colores compartidos para temas claro/oscuro. Son un primer reconocimiento del proyecto: navegación y estilos avanzados se consultan en [Unidad 3](03_UNIDAD_3.md), sin desarrollarlos de nuevo aquí. **Fuente: Clase 20/08/2026, 18:11–48:22.**

### Contenido web y precisiones de estructura

La clase distingue una **WebView**, que integra contenido web dentro de una vista de la aplicación, de **`expo-web-browser`**, que utiliza la experiencia de navegador del sistema. El contraste evita tratar ambas opciones como si fueran el mismo componente. **Fuente: Clase 20/08/2026, 18:11–48:22, según los aportes recibidos; contraste local: Seguridad, pp. 25–27, documentadas en Unidad 6.**

**Precisiones editoriales contrastadas con los materiales locales:**

- Los paréntesis indican un **grupo de rutas**, no pestañas por sí solos; el navegador se define mediante el layout. **Navegación, pp. 4, 8 y 14, en Unidad 3.**
- `slug` no debe confundirse con `android.package` o `ios.bundleIdentifier`, identificadores de las plataformas. **Permisos, p. 14, y Publicación, p. 6, documentadas en unidades 4 y 7.**
- `assets` no es una obligación de ubicación única; tampoco se descarta `src/`: los PDF muestran rutas como `src/app/`. **Testing, pp. 9–10; Navegación, p. 4.**

Estas precisiones evitan convertir simplificaciones orales en reglas universales de estructura.

## 1. TypeScript: tipos antes de ejecutar

TypeScript agrega un sistema de tipos a JavaScript. La comprobación ocurre antes de ejecutar; los tipos desaparecen al transformar el código y no realizan validaciones por sí mismos en el dispositivo. El material destaca que se puede adoptar de manera gradual y que la plantilla de Expo utilizada en la clase ya viene preparada. Su valor consiste en detectar errores mientras se escribe, antes de que lleguen al usuario. **Fuente: React, pp. 4–5.**

### Tipos, inferencia e interfaces

Se pueden anotar `string`, `number`, `boolean`, arreglos y retornos, pero muchas veces TypeScript los infiere a partir de los valores. La presentación recomienda explicitar parámetros y contratos de datos externos. **Fuente: React, p. 6.**

```ts
interface Producto {
  id: number;
  nombre: string;
  precio: number;
  descripcion?: string;
}

interface PropsTarjeta {
  producto: Producto;
  alTocar: (id: number) => void;
}
```

Una interfaz documenta la forma del objeto; `?` señala un campo opcional. En React se utiliza especialmente para describir las props y los eventos que recibe un componente. **Fuente: React, p. 7.**

La clase practica tipado explícito e inferencia con datos de personas/usuarios, lugares y códigos QR. Las interfaces describen las propiedades esperadas de cada entidad y el editor ayuda a detectar incompatibilidades entre valores y tipos. **Fuente: Clase 20/08/2026, 48:59–1:08:27, según los aportes recibidos.** Como el listado no detalla todos los campos originales, no se inventan sus esquemas exactos.

**Ejemplo editorial mínimo para interpretar esas comprobaciones:** asignar un número a una propiedad declarada `string` o pasar un objeto incompatible con una interfaz produce un diagnóstico de tipos. El uso de `any` elimina comprobaciones en las operaciones sobre ese valor; no es obligatorio usarlo por desconocer inicialmente la forma del dato. Tampoco se afirma que cualquier proyecto Expo bloquee automáticamente su ejecución ante todo error TypeScript: un diagnóstico del editor y el comportamiento de la herramienta de ejecución son cuestiones distintas. **Contraste: React, pp. 4–9.**

### Uniones y genéricos

Una unión permite representar alternativas de un mismo estado, incluyendo los datos que corresponden a cada caso:

```ts
type Estado =
  | { fase: 'cargando' }
  | { fase: 'listo'; productos: Producto[] }
  | { fase: 'error'; mensaje: string };

function render(estado: Estado) {
  if (estado.fase === 'cargando') return 'Cargando…';
  if (estado.fase === 'error') return estado.mensaje;
  return estado.productos.length + ' productos';
}
```

Al discriminar por `fase`, el compilador puede determinar en qué rama existe `productos`. Esto expresa mejor la relación entre carga, éxito y error que varios valores independientes sin restricciones. **Fuente: React, p. 8.**

Los genéricos convierten el tipo en un parámetro reutilizable. El ejemplo `traer<T>(url: string): Promise<T>` usa `fetch` y devuelve `respuesta.json()`; se invoca con `traer<Producto[]>('/api/productos')` o con otro tipo. **Fuente: React, p. 9.**

**Aclaración editorial:** ese genérico expresa un contrato para el compilador; no comprueba que el JSON recibido cumpla la interfaz. Asimismo, los ejemplos con rutas `/api/...` son ilustrativos: no establecen por sí solos la dirección de un servidor accesible desde un teléfono.

### Refactor de respuestas con `Respuesta<T>`

En la clase se parte de respuestas específicas para distintas entidades y se extrae una interfaz de paginación compartida. Después se concentra el formato repetido en **`Respuesta<T>`**, con una colección `data: T[]` y la paginación. Cambiar `T` permite mantener el mismo contrato exterior para usuarios, lugares o códigos QR. **Fuente: Clase 20/08/2026, 48:59–1:08:27, según los aportes recibidos.**

```ts
interface Respuesta<T> {
  data: T[];
  paginacion: Paginacion;
}
```

**Reconstrucción didáctica basada en la explicación oral**, no copia exacta del código mostrado. `Paginacion` representa la interfaz compartida del ejemplo; sus campos concretos no están especificados en el listado y no se inventan. Tampoco se reproducen interfaces distintas para cada entidad solo para repetir esta estructura.

La ventaja del refactor es expresar una única vez lo común y comprobar que cada uso mantenga el tipo de sus elementos. Esta forma `data`/`paginacion` pertenece al ejemplo, **no a todas las APIs**. Se conserva además el límite ya explicado: declarar `Respuesta<Lugar>` no valida en ejecución el JSON que el servidor devuelva.

## 2. React: interfaz declarativa, componentes y flujo de datos

React permite describir cómo debe verse la interfaz para un estado dado. Frente a modificar manualmente un nodo y sus clases, el ejemplo declara un `Text` cuyo estilo depende de la cantidad de elementos del carrito. La idea es mantener una fuente de verdad y derivar la interfaz de ella. **Fuente: React, p. 11.**

Un componente funcional devuelve JSX, puede contener otros componentes y utiliza un nombre en PascalCase. Si devuelve varios hermanos, los agrupa con un contenedor o un fragmento `<>...</>`. JSX no es HTML: representa llamadas que construyen elementos; con TypeScript se escribe en archivos `.tsx`. **Fuente: React, pp. 12–13.**

### Elementos web, componentes nativos y composición

La clase introduce de forma práctica estos componentes:

| Componente | Papel en la interfaz |
| --- | --- |
| `View` | Contener y organizar otros componentes. |
| `Text` | Mostrar texto. |
| `TextInput` | Recibir entrada de texto. |
| `Image` | Mostrar una imagen. |
| `Pressable` | Responder a la interacción de pulsación. |

**Fuente: Clase 20/08/2026, 1:09:22–1:18:41; contraste: Interfaz, pp. 4–8 y 14, documentadas en Unidad 3.** La comparación con etiquetas web orienta, pero no convierte estos componentes en elementos del DOM. React Native sí dispone de `Button`, que también aparece en los ejemplos del PDF React, pp. 15 y 28; usar `Pressable` no demuestra que no exista un botón.

Para componer una pantalla se reutilizan componentes y se agrupan hermanos cuando hace falta. `View` crea un contenedor nativo; un fragmento `<>...</>` agrupa elementos React sin añadir ese contenedor. **Aclaración editorial:** un fragmento no es un `span`, que es un elemento HTML. `.tsx` identifica TypeScript con JSX; su `x` no significa «native ejecutable». **Fuentes: React, pp. 12–13; Clase 20/08/2026, 1:09:22–1:18:41.**

Este tramo amplía la cobertura práctica de componentes nativos frente a elementos web. No desarrolla en profundidad la arquitectura de ejecución de React Native.

### Props y estado

| Props | Estado |
| --- | --- |
| Llegan desde el padre. | Se mantiene dentro del componente. |
| Son de solo lectura para quien las recibe. | Se modifica mediante su función de actualización. |
| Cambian cuando el padre proporciona otros valores. | Su actualización provoca un nuevo renderizado. |

**Fuente: React, pp. 14 y 16.**

Los datos bajan y los eventos suben: el hijo recibe una función, por ejemplo `aBorrar(id)`, y avisa que se pulsó un botón. El padre decide cómo cambiar el arreglo, usando en el ejemplo `setItems(xs => xs.filter(x => x.id !== id))`. Así, la fila no necesita conocer toda la lógica de la lista. **Fuente: React, p. 15.**

### Ejemplo de clase: `Titulo`, extracción y callback

La demostración crea un componente funcional, define una interfaz con **`titulo: string`**, recibe y desestructura las props, muestra `{titulo}` en JSX y pasa el texto desde el padre. También distingue propiedades obligatorias y opcionales mediante `?`. **Fuente: Clase 20/08/2026, 1:18:41–1:23:40, según los aportes recibidos.**

Después trabaja estilos como objetos, `StyleSheet`, propiedades en camelCase y aplicación mediante `style`. El componente se traslada a **`components/ui`** y se exporta/importa para reutilizarlo. La clase diferencia `Text` nativo del componente de texto con soporte de temas de la plantilla: ese comportamiento adicional pertenece al componente de la plantilla, no se obtiene por cambiar el nombre del `Text` básico. **Fuente: Clase 20/08/2026, 1:23:47–1:34:39.**

Por último, el padre proporciona una función y el hijo la invoca al recibir `onPress`. Un callback sin parámetros ni valor devuelto se expresa como `() => void`; si es opcional, se comprueba antes de invocarlo. **Fuente: Clase 20/08/2026, 1:34:51–1:39:45.**

```tsx
// components/ui/Titulo.tsx
import { Pressable, StyleSheet, Text } from 'react-native';

interface PropsTitulo {
  titulo: string;
  alPresionar?: () => void;
}

export default function Titulo({ titulo, alPresionar }: PropsTitulo) {
  return (
    <Pressable onPress={() => alPresionar?.()}>
      <Text style={estilos.titulo}>{titulo}</Text>
    </Pressable>
  );
}

const estilos = StyleSheet.create({
  titulo: { fontWeight: 'bold' },
});
```

```tsx
// Fragmento del componente padre
import Titulo from './components/ui/Titulo';

<Titulo titulo="Mi ciudad" alPresionar={() => console.log('Título presionado')} />
```

**Reconstrucción didáctica basada en la explicación oral** de los tres tramos, no copia exacta del código mostrado. El nombre `alPresionar`, el estilo, el mensaje y la ruta relativa del import son elecciones editoriales mínimas; la ruta presupone un padre junto a `components/` y debe ajustarse a su ubicación real. El fragmento del padre no es por sí solo un archivo de pantalla completo.

La función también **baja como prop**: la secuencia es **interacción → manejador del hijo → callback del padre**. El hijo notifica ejecutando una función que recibió; no modifica por su cuenta las props del padre.

**Precisión editorial de estilos:** las medidas numéricas del layout no se equiparan a píxeles físicos ni se asume compatibilidad con todas las unidades y atajos de CSS. Interfaz, pp. 24–25, desarrolla los objetos de estilo y las unidades independientes de densidad. Para temas, estilos avanzados y navegación, consultar [Unidad 3](03_UNIDAD_3.md).

Si un dato puede calcularse a partir de props o de otro estado, la recomendación es calcularlo al renderizar. Duplicarlo introduce dos fuentes de verdad que pueden desincronizarse. **Fuente: React, p. 16.**

### Listas y organización

Las listas se construyen con `map` y una `key` estable, como `producto.id`. Usar la posición de una fila como identidad puede asociar su estado con otro producto cuando se borra o reordena la colección. El material recomienda componentes pequeños, con propósito claro, nombres descriptivos, props tipadas y cálculos fuera del JSX. **Fuente: React, pp. 17–18.**

## 3. Hooks

Un componente vuelve a ejecutarse cuando React necesita renderizarlo. Los hooks permiten conservar estado, referencias y relaciones con sistemas externos entre esas ejecuciones. La presentación compara este modelo con el uso anterior de clases y `this.state`. **Fuente: React, p. 20.**

Las reglas generales son llamarlos en el nivel superior y hacerlo desde componentes o hooks propios. No se colocan en bucles, condiciones, manejadores ni funciones comunes: el orden de llamadas debe mantenerse entre renderizados. **Fuente: React, p. 21.**

### `useState`: cada renderizado tiene su valor

```tsx
const [cantidad, setCantidad] = useState(0);
const [productos, setProductos] = useState<Producto[]>([]);

setCantidad(c => c + 1);
setCantidad(c => c + 1);
```

La forma funcional encadena actualizaciones sobre el valor anterior. En cambio, dos llamadas a `setCantidad(cantidad + 1)` en el mismo contexto leen el mismo valor del renderizado y no equivalen a sumar dos. Llamar al setter no modifica inmediatamente la constante local. **Fuente: React, p. 22.**

### `useEffect`: sincronización y limpieza

```tsx
useEffect(() => {
  const id = setInterval(() => console.log('tic'), 1000);
  return () => clearInterval(id);
}, []);
```

El efecto inicia una actividad y su retorno la limpia. Con dependencias se vuelve a sincronizar cuando cambian; sin arreglo se ejecuta después de cada renderizado. El arreglo vacío expresa que no depende de valores reactivos cambiantes del componente. **Fuente: React, p. 23.**

La explicación más precisa de la clase es pensar en **empezar y dejar de sincronizar**: si cambia `salaId`, primero se cancela la suscripción anterior y después se crea la nueva. No se deben quitar dependencias para silenciar ejecuciones, porque el efecto puede quedar leyendo valores viejos. **Fuente: React, pp. 35–36 y 42.**

### Elegir el hook según el problema

| Hook | Para qué se utiliza en la fuente | Referencia React |
| --- | --- | --- |
| `useContext` | Leer datos compartidos por una parte del árbol: tema, sesión, idioma. | p. 24 |
| `useRef` | Conservar un valor sin renderizar o acceder imperativamente a un campo, scroll o reproductor. | p. 25 |
| `useMemo` | Memorizar un resultado calculado. | p. 26 |
| `useCallback` | Mantener la identidad de una función cuando sus dependencias no cambian. | p. 26 |
| `useReducer` | Concentrar transiciones de estado en una función. | p. 28 |
| Hook propio | Reutilizar lógica, no interfaz, componiendo otros hooks. | p. 29 |

Si un valor debe reflejarse en pantalla, guardarlo solamente en `ref.current` no alcanza: cambiarlo no solicita un renderizado. Los ejemplos incluyen enfocar un `TextInput` mediante `campo.current?.focus()`. La memorización tiene costo y no se agrega sin una necesidad identificada. **Fuente: React, pp. 25–26.**

En el ejemplo de reducer, las acciones `sumar`, `restar` y `reiniciar` determinan el siguiente número. El hook propio `useContador` devuelve `valor`, `sumar` y `reiniciar`; las pantallas reutilizan esa lógica sin copiarla. **Fuente: React, pp. 28–29.**

En la clase del 27/08, la consulta sobre `useReducer` no conduce a una explicación detallada adicional. Se conserva la del PDF y la indicación de **no forzar el uso de todos los hooks del repaso**: se eligen según las necesidades de la implementación. **Fuente: Clase 27/08/2026, 52:02–58:09, según los aportes recibidos.**

### React Compiler y novedades que presenta la clase

La presentación describe React Compiler como una optimización de memorización durante la construcción y muestra en `app.json`:

```json
{ "expo": { "experiments": { "reactCompiler": true } } }
```

También menciona `npx react-compiler-healthcheck`, reglas de ESLint y la directiva `'use no memo'`. La condición es respetar las reglas de React; no reemplaza corregir mutaciones indebidas. **Fuente: React, p. 27.**

Para el contexto de React 19/19.2 de la clase se presentan `ref` como prop, el contexto como proveedor directo, `use()` para leer contexto o promesas —con la excepción a la regla de llamadas condicionales que indica la diapositiva—, `useEffectEvent` para leer valores actuales sin convertirlos en disparadores de un efecto y `Activity` para ocultar contenido conservando estado. **Fuente: React, pp. 30–31.**

**Aclaración editorial:** se documenta lo expuesto para las versiones declaradas por el PDF; no se activó el compilador ni se validó compatibilidad en una aplicación concreta.

## 4. Los tres ciclos de vida

### Componente

El componente se monta, se actualiza por cambios de props o estado y se desmonta. Los hooks permiten reaccionar a esas situaciones, pero no son una traducción exacta de los métodos de clases. La tabla con `componentDidMount`, `componentDidUpdate` y `componentWillUnmount` sirve para leer código heredado. **Fuente: React, pp. 33–35.**

En desarrollo, Strict Mode realiza comprobaciones adicionales que ponen a prueba la limpieza. La presentación utiliza el ciclo de montaje, desmontaje y montaje para explicar por qué pueden verse efectos repetidos. La propuesta es corregir la sincronización y la limpieza, no ocultar el problema retirando el modo estricto. **Fuente: React, p. 37.**

### Pantalla

Una pantalla puede seguir montada al navegar a otra. Por eso, montaje no equivale a cada entrada del usuario. Para una tarea que debe mantenerse solo mientras la pantalla tiene foco se utiliza `useFocusEffect`:

```tsx
useFocusEffect(
  useCallback(() => {
    const id = setInterval(refrescarSaldo, 5000);
    return () => clearInterval(id);
  }, [])
);
```

El callback estable evita reiniciar el efecto por una identidad nueva en cada renderizado. **Fuente: React, pp. 38–39.**

### Aplicación

`AppState` informa transiciones de la app: `active`, `background` e `inactive` en iOS. El ejemplo registra un listener, refresca al volver a `active` y lo elimina con `sub.remove()`. Una app en primer plano no implica que una pantalla particular tenga foco, ni salir de una pantalla implica desmontarla. **Fuente: React, pp. 40–41.**

Antes de escribir un efecto conviene determinar qué ciclo corresponde: **componente → `useEffect`; pantalla → `useFocusEffect`; aplicación → `AppState`**. Los errores destacados son no limpiar, quitar dependencias, esperar remontajes y utilizar efectos para estado que se podría derivar durante el renderizado. **Fuente: React, pp. 41–42.**

## 5. Testing: comprobar comportamientos

La clase del 27/08 menciona los tests unitarios y difiere su tratamiento práctico. Esto no reduce la cobertura teórica disponible: se conserva a continuación el desarrollo de unidad, integración y E2E, con los ejemplos y referencias del PDF. **Fuente del anuncio: Clase 27/08/2026, 52:02–58:09.**

Un test es una red para cambios futuros y documentación ejecutable de lo esperado. No garantiza por sí solo que toda la app funcione. La clase propone probar lo que el usuario percibe y lo que puede romperse: cálculos propios, validaciones, estados vacíos o de error y errores ya detectados. Desaconseja comprobar detalles internos o estilos exactos sin un propósito de comportamiento. **Fuente: Testing, pp. 4 y 6.**

| Escala | Qué comprueba | Herramientas de la clase |
| --- | --- | --- |
| Unidad | Una función o un componente aislado. | Jest y Testing Library. |
| Integración | Piezas relacionadas, como pantalla, navegación y datos. | `expo-router/testing-library`. |
| E2E | Aplicación instalada y recorridos de usuario. | Maestro. |

Se proponen muchos tests de unidad, algunos de integración y pocos E2E, por su costo y mantenimiento. **Fuente: Testing, p. 5.**

### Preparación y primer ejemplo

```bash
npx expo install jest-expo jest @types/jest --dev
npx expo install @testing-library/react-native --dev
```

El preset `jest-expo` simula la parte nativa del SDK. La configuración mostrada agrega `"jest": { "preset": "jest-expo" }` y un script de ejecución en `package.json`, y `"types": ["jest"]` dentro de `compilerOptions` en `tsconfig.json`. Son fragmentos a integrar en la configuración existente. **Fuente: Testing, p. 8.**

```tsx
import { render, screen } from '@testing-library/react-native';
import Inicio from '@/app/index';

test('saluda al abrir', () => {
  render(<Inicio />);
  expect(screen.getByText('¡Bienvenida!')).toBeVisible();
});
```

El componente de ejemplo presenta ese saludo. El test prepara la vista y comprueba lo visible. Los tests de pantallas van fuera de `app/`, por ejemplo en `__tests__/inicio-test.tsx`, para que Expo Router no los interprete como rutas. **Fuente: Testing, pp. 9–10.**

### Consultas, interacción y asincronía

Se busca por texto, etiqueta accesible, placeholder o rol. `getBy...` exige que el elemento exista; `queryBy...` permite comprobar su ausencia; `findBy...` espera su aparición. **Fuente: Testing, p. 11.**

```tsx
test('muestra el error si el campo está vacío', async () => {
  const usuario = userEvent.setup();
  render(<Formulario />);
  await usuario.press(screen.getByText('Enviar'));
  expect(await screen.findByText('El nombre es obligatorio')).toBeVisible();
});
```

El ejemplo sigue **preparar → actuar → verificar**. `Formulario` es el componente supuesto por la diapositiva y `userEvent` se importa desde Testing Library. **Fuente: Testing, p. 12.**

### Instantáneas, cobertura y ejecución

Los snapshots guardan el árbol renderizado y comparan cambios con `toMatchSnapshot()`; `jest -u` los actualiza. La clase recomienda utilizarlos con moderación porque aceptar cambios sin revisar anula su valor. **Fuente: Testing, p. 13.**

La p. 14 propone scripts separados: `jest --watch --changedSince=origin/main` durante el trabajo, `jest` para la ejecución completa y `jest -u` para regenerar instantáneas. La cobertura se configura con `collectCoverage` y `collectCoverageFrom`; el informe está en `coverage/lcov-report/index.html` y la carpeta generada se excluye del versionado. Sirve para localizar código no ejercitado, no para sustituir la calidad de las verificaciones por un porcentaje. **Fuente: Testing, p. 14.**

La presentación señala `react-test-renderer` como material antiguo para su entorno y utiliza `@testing-library/react-native`. Se conserva esa indicación del PDF sin realizar aquí una migración de dependencias. **Fuente: Testing, p. 15.**

### Navegación, E2E y TDD

El ejemplo de integración utiliza `renderRouter` y `toHavePathname` para abrir `/productos/12`. Maestro usa YAML para lanzar la app, verificar «¡Bienvenida!», tocar «Explorar» y buscar la pantalla de productos:

```yaml
appId: ar.edu.uner.miapp
---
- launchApp
- assertVisible: '¡Bienvenida!'
- tapOn: 'Explorar'
- assertVisible: 'Productos.*'
```

Se ejecuta con `maestro test .maestro/inicio.yml`; la fuente menciona EAS Workflows como alternativa de ejecución en la nube. **Fuente: Testing, pp. 17–18.**

`npx expo lint` y TypeScript agregan controles estáticos. TDD propone **rojo** —test que falla—, **verde** —implementación mínima— y **refactor** —ordenar conservando el comportamiento—. Se destaca reproducir un bug con un test antes de corregirlo. Para el integrador, la prioridad indicada es lint y tipos, lógica propia, componentes condicionales y un recorrido principal E2E. **Fuente: Testing, pp. 19–21.**

## 6. Depuración

La demostración práctica de depuración se posterga en la clase del 27/08. Se registra como límite de cobertura audiovisual y se conserva íntegro el desarrollo del PDF a continuación, sin afirmar que esas herramientas se hayan demostrado en esa grabación. **Fuente: Clase 27/08/2026, 52:02–58:09.**

El menú de desarrollo, LogBox, Fast Refresh y DevTools pertenecen al entorno de debug. No se espera que aparezcan en release. Desde la terminal, `m` abre el menú y `j` las DevTools. La presentación enumera también gestos y atajos por plataforma. **Fuente: Depuración, pp. 4–6.**

React Native DevTools se presenta como la experiencia de depuración para el entorno Hermes de la clase. El material advierte sobre tutoriales basados en Flipper, `chrome://inspect` o Remote JS Debugging. **Fuente: Depuración, p. 8.**

| Panel o recurso | Qué permite observar | Página de Depuración |
| --- | --- | --- |
| Console | Ejecutar expresiones, filtrar logs y conservarlos entre recargas. | 9 |
| Sources y breakpoints | Pausar, inspeccionar variables, pila y condiciones de ejecución. | 10 |
| Network / Expo Network | Requests, tiempos, cabeceras, respuesta y origen de la llamada. | 11 |
| Components | Árbol React, props y estado; no es el árbol de vistas nativas. | 12 |
| Highlight updates | Detectar qué componentes se renderizan al interactuar. | 13 |
| Profiler | Tiempo y cantidad de renderizados. | 14 |
| Memory | Comparar instantáneas para investigar retenciones o fugas. | 14 |

Un `debugger;` o un breakpoint condicional permite observar el contexto del error sin multiplicar logs. Comparar snapshots de memoria ayuda a investigar, por ejemplo, efectos que dejaron listeners abiertos. **Fuente: Depuración, pp. 10 y 14.**

## 7. Rendimiento: medir antes de optimizar

La clase utiliza una referencia de 60 cuadros por segundo: cada cuadro dispone de aproximadamente **16,67 ms**. Una tarea de 200 ms puede hacer perder unos 12 cuadros. La pregunta útil es qué operación supera el presupuesto de tiempo, no afirmar que toda la app es lenta. **Fuente: Depuración, p. 16.**

Se distinguen el **hilo de JavaScript**, donde corre la lógica de la aplicación, y el **hilo de UI**, responsable del trabajo nativo de interfaz. Un desplazamiento nativo puede continuar aunque JS esté ocupado; observar ambos FPS ayuda a localizar el problema. Perf Monitor muestra memoria, vistas y FPS, pero introduce su propio costo. **Fuente: Depuración, pp. 17–18.**

**Importante para interpretar la fuente:** el rendimiento percibido final se verifica en un dispositivo real con release. Las herramientas que el PDF indica como exclusivas de debug sirven para diagnóstico y comparación, no para atribuir a release sus tiempos absolutos. **Fuente: Depuración, pp. 4, 14 y 18–22.**

Los casos destacados son:

- Listas largas: `ScrollView` con `map` crea todos los hijos; `FlatList` virtualiza. Con filas de altura conocida, `getItemLayout` evita mediciones. **Depuración, p. 20.**
- Logs excesivos: el material propone retirar `console.*` de producción con un plugin de Babel; no aporta aquí una configuración completa. **Depuración, p. 19.**
- Animaciones: se menciona `useNativeDriver` en Animated y animar escala en lugar de redimensionar imágenes. **Depuración, p. 21.**
- Respuesta al toque: evitar trabajo pesado en el mismo instante del feedback; la diapositiva menciona `requestAnimationFrame`. **Depuración, p. 21.**

El procedimiento es **reproducir → medir → cambiar una cosa → volver a medir**. La memorización sin evidencia puede sumar complejidad sin mejorar el problema real. **Fuente: Depuración, p. 22.**

## Cierre y limitaciones de cobertura

- Los tres PDF disponibles quedaron integrados, con sus conceptos y ejemplos principales.
- **Estado audiovisual: 2 de 2 videos incorporados**, clases del 20/08/2026 y 27/08/2026. El usuario confirma que el segundo es el último; no quedan búsquedas abiertas de más videos por anuncios de las grabaciones.
- El usuario indica que la transcripción automática del primer video llega a **1:47:56**. Se conserva el límite del listado recibido y no se reconstruye el tramo final sin aportes detallados.
- La primera clase aporta creación/estructura de proyecto, tipado, componentes nativos, props, estilos básicos y comunicación por callbacks; no reemplaza la teoría de hooks, ciclo de vida, testing y rendimiento de los PDF.
- React, pp. 2 y 43, anuncia una clase sobre arquitectura y Expo. Se registra el anuncio como referencia temática, **no como evidencia de un tercer video**.
- La segunda clase amplía la lectura del PRD, el desarrollo con mocks/servicios y las orientaciones de entrega y defensa. La transcripción automática recibida, según lo informado, se corta a los **59:58 en medio de una intervención**; no se afirma que la grabación termine allí y no se reconstruye lo no recibido.
- **Arquitectura/Hermes:** en el segundo video hay solo un comentario contextual —02:23–03:31— y referencias durante el intercambio de 52:02–58:09. No constituye desarrollo profundo de arquitectura. Esta limitación se registra sin bloquear el cierre ni abrir una búsqueda de otro video.
- **Práctica de depuración y testing:** la demostración de depuración se posterga y los tests unitarios se difieren. La teoría y los ejemplos de ambos PDF permanecen integrados; el aplazamiento audiovisual no bloquea el cierre.
- **`useReducer`:** la consulta no añade un desarrollo detallado; se conserva el del PDF. No es obligatorio utilizar todos los hooks solo porque aparezcan en el repaso.
- El PRD turístico es un caso didáctico elaborado con IA, no un relato verificado ni una consigna universal. Los posibles recortes de alcance se registran como propuestas y la transcripción no sustituye al PRD completo. Las APIs anunciadas no se dan por entregadas.

La Unidad 2 queda como **Documentación completa respecto del material disponible**, con **2 de 2 audiovisuales incorporados** y los límites anteriores. No se desarrolla multitenancy, expresamente fuera del alcance práctico señalado en la clase, ni se incorpora la conversación final sobre precios.
