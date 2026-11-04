# Unidad 3 — Interfaz, temas, accesibilidad y navegación

[Volver al índice](00_INDICE.md)

**Estado: Audiovisuales completos; pendiente la integración del texto independiente de Context.** **5 de 5 videos incorporados:** 03/09/2026, «Navegación» sin fecha informada, 10/09/2026, 17/09/2026 y 01/10/2026. Se conservan los dos PDF y las incorporaciones anteriores. No quedan videos por recibir. El texto «Context en React: compartir datos con todo el árbol» no está disponible entre las fuentes locales consultadas; su estado se mantiene separado y no se considera sustituido por la práctica audiovisual.

## Fuentes y alcance

| Referencia     | Fuente original                                                                                                   | Páginas |
| -------------- | ----------------------------------------------------------------------------------------------------------------- | ------- |
| **Interfaz**   | [U03 T02 - Interfaz y navegación.pdf](../fuentes/pdf/U03%20T02%20-%20Interfaz%20y%20navegacio%CC%81n.pdf)         | 43      |
| **Navegación** | [U03 T01 - Navegación - Expo Router.pdf](../fuentes/pdf/U03%20T01%20-%20Navegacio%CC%81n%20-%20Expo%20Router.pdf) | 22      |

El programa, p. 3, incluye construcción de pantallas, componentes, StyleSheet y estilos en línea, Styled Components, temas, diseño responsivo, gestos, teclado, pull-to-refresh, Expo Router, patrones y protección de rutas. Los apuntes integran los PDF por tema. Las páginas son las del visor, incluida la portada. Los fragmentos conservan el contexto de las fuentes y no son aplicaciones completas ni instalaciones verificadas.

**Fuente audiovisual incorporada:** «GRABACIÓN CLASE UNIDAD III - 03/09/2026», primer video de los cinco confirmados por el usuario. Fuente identificada como transcripción automática que llega hasta **1:55:20 e incluye la despedida**. Enlace no proporcionado: no se inventa ni se reutiliza uno de otras clases.

**Segunda fuente audiovisual incorporada:** video 2, **«Navegación»**, transcripción automática aportada por el usuario, con despedida en **37:34**. No se proporcionaron fecha ni enlace. Las referencias **Video 2 — Navegación** identifican esta fuente y no se le atribuye la fecha del video 1. La integración utiliza el listado de aportes y marcas recibido, sin afirmar una revisión directa del video ni reconstruir código literal ausente.

**Tercera fuente audiovisual incorporada:** clase del **10/09/2026**, video 3 de 5. La transcripción identificada por el usuario termina a **1:36:18 en medio de una frase**; no se afirma que la grabación termine allí. No se proporcionó enlace. Se integran los aportes y tiempos recibidos, sin reconstruir el texto no disponible ni atribuir una revisión directa del video. Los límites aproximados de los tramos se conservan como tales.

**Cuarta fuente audiovisual incorporada:** clase del **17/09/2026**, video 4 de 5. El usuario identifica una transcripción que llega hasta **1:59:21 e incluye la despedida**. No se proporcionó enlace. Se integran los aportes y tiempos recibidos, sin atribuir una revisión directa del video ni una copia literal de código no disponible. Los intervalos señalados como aproximados conservan ese carácter.

**Quinta fuente audiovisual incorporada:** clase del **01/10/2026**, video 5 de 5. El usuario informa que la transcripción llega a **1:28:27 e incluye el cierre**. No se proporcionó enlace a la grabación. Se integran los aportes y marcas recibidos, sin afirmar una revisión directa del video ni disponer de su código literal. La práctica completa el desarrollo de Context anunciado el 17/09, pero no reemplaza la fuente escrita independiente.

**Alcance de la incorporación:** el adjunto recibido contiene aportes y marcas de tiempo, no el cuerpo literal completo de los subtítulos. Se integra lo respaldado por ese listado sin atribuir una revisión directa del video. Los ejemplos nuevos se identifican como reconstrucciones didácticas. Versiones y plazos relativos conservan el contexto de la clase y no se convierten en requisitos actuales ni fechas definitivas.

### Indicaciones de cursada del 03/09/2026

Se recuerda la inscripción en grupos, la elección de uno de los PRD disponibles y la posibilidad de consultar temáticas alternativas. Se pide acordar **una misma versión del SDK entre integrantes** para trabajar sobre una base común. Para comenzar con Expo Go **no se exige emulador**. Son indicaciones de esa fecha, sin fijar desde ellas una versión actual obligatoria ni convertir plazos relativos de la conversación en fechas definitivas. **Fuente: Clase 03/09/2026, 00:41–06:28, según los aportes recibidos.**

### Aclaraciones de cursada del 01/10/2026

**Orientación de evaluación del 01/10:** el docente espera que cada estudiante pueda explicar cómo funciona un componente y justificar por qué lo eligió. La consulta sobre notificaciones push describe conceptualmente el recorrido **dispositivo → servidor de la app → Expo**; no se implementa ese circuito en esta clase ni se lo presenta como una integración completa de entrega de notificaciones. **Fuente: Clase 01/10/2026, aproximadamente 02:29–15:15.**

### Del PRD a las pantallas: cooperativa de agua

La clase del 10/09 presenta un **caso didáctico del docente** para una cooperativa de agua. Las pantallas mostradas son **maquetas**: permiten recorrer una propuesta de interfaz y no demuestran por sí mismas que las funcionalidades estén implementadas. Cada grupo sigue trabajando sobre **su propio PRD**, no queda obligado a reemplazarlo por este ejemplo. **Fuente: Clase 10/09/2026, 02:53–16:21, según los aportes recibidos.**

El recorrido del lector de medidores es:

1. Descargar la ruta de trabajo.
2. Consultar los suministros en el orden previsto.
3. Identificar el medidor mediante QR.
4. Registrar una lectura o una novedad.
5. Pasar al siguiente suministro.
6. Al cerrar la ruta, advertir si quedan lecturas sin subir.

El PRD pide **trabajar sin señal y sincronizar al recuperar conexión**. Mapas, fotos, notas de voz y videos instructivos forman parte del diseño presentado. La advertencia de lecturas pendientes debe distinguir el cierre del recorrido de la confirmación de que todos los datos llegaron al servidor. **Fuente: Clase 10/09/2026, 02:53–16:21.**

**Aclaración editorial para estudiar las maquetas:** la secuencia vincula las pantallas con tareas y estados del trabajo. Una ruta descargada, una lectura registrada localmente y una lectura sincronizada no equivalen a lo mismo. Esto organiza los requisitos recibidos, sin agregar una implementación de persistencia, sincronización o backend a la demostración.

### Orientaciones de diseño de los PRD: preparar el uso sin señal

En las consultas del 17/09 se propone definir **qué recorrido o datos necesitará el usuario antes de perder señal**, guardar localmente lo que produzca durante el trabajo sin conexión y enviarlo cuando vuelva internet. La preparación previa y el registro de operaciones pendientes son decisiones del diseño; no basta con mostrar una pantalla que funciona mientras hay red. **Fuente: Clase 17/09/2026, 1:46:20–1:59:21, según los aportes recibidos.**

La decisión de mostrar un mapa depende del caso de uso y de lo que necesite hacer la persona. Estas respuestas se registran como **orientaciones de diseño para los PRD**, sin convertirlas en una integración offline ya implementada ni en una exigencia idéntica para todos los proyectos. APIs, permisos y notificaciones se anuncian para **Unidad 4**; el anuncio no desarrolla esas integraciones en esta clase. **Fuente: Clase 17/09/2026, 1:46:20–1:59:21.**

## 1. Componentes para construir pantallas

React Native utiliza componentes que representan capacidades de la plataforma. La presentación parte de cuatro componentes básicos: `View`, `Text`, `TextInput` y `Pressable`. **Fuente: Interfaz, p. 4.**

### Contenedores y texto

`View` organiza hijos con Flexbox y dirección inicial `column`. `onLayout` permite conocer su posición y tamaño calculados; `pointerEvents` controla cómo se distribuyen los toques entre contenedor e hijos; `hitSlop` amplía el área sensible sin modificar el tamaño visual y dentro de los límites del padre. Las props de rol y etiqueta describen el elemento para el lector de pantalla. **Fuente: Interfaz, p. 5.**

Todo texto visible debe estar dentro de `Text`. Su disposición es de texto, no la de una caja Flexbox. Los `Text` anidados permiten combinar formatos dentro de un párrafo. `numberOfLines` limita líneas y `ellipsizeMode` define el recorte. La fuente recomienda conservar el escalado tipográfico del sistema y considerar `maxFontSizeMultiplier` si hace falta acotarlo. **Fuente: Interfaz, pp. 4 y 6.**

La clase relaciona `View` con vistas nativas del sistema y diferencia ese modelo de una interfaz basada en WebView. La semejanza de uso con un contenedor web no significa que se esté dibujando HTML en un navegador embebido. **Fuente: Clase 03/09/2026, 07:12–34:38, según los aportes recibidos.**

Se amplía `pointerEvents` con cuatro modalidades:

| Valor | Distribución de los toques |
| --- | --- |
| `auto` | Comportamiento habitual: pueden recibirlos la vista y sus hijos. |
| `none` | Ni la vista ni sus hijos reciben los toques. |
| `box-none` | La vista no los recibe, pero sus hijos pueden recibirlos. |
| `box-only` | La vista puede recibirlos y sus hijos no. |

**Fuentes: Clase 03/09/2026, 07:12–34:38; Interfaz, p. 5.** La elección permite decidir cómo interactúan contenedores y controles superpuestos, sin confundir el tamaño visual con el área sensible.

En los ejemplos de texto se combinan formatos con `Text` anidados, se interpolan valores mediante `{...}` y se acortan descripciones con `numberOfLines` y `ellipsizeMode`. El escalado de fuente responde a las preferencias del usuario; no debe interpretarse el tamaño observado en la demostración como un resultado fijo en todos los teléfonos. **Fuente: Clase 03/09/2026, 07:12–34:38.**

**Aclaración del propio docente, 30:52–31:18:** un componente puede devolver **solamente un `Text`**; no necesita obligatoriamente un `View`. Cuando se devuelven varios hermanos sí se requiere agrupación, mediante un contenedor o un fragmento según se necesite o no una vista adicional. Esta precisión evita convertir los contenedores usados en la demostración en una obligación para todo componente.

### Entrada y respuesta al toque

`TextInput` puede manejarse de forma controlada: el valor vive en estado, vuelve mediante `value` y se actualiza con `onChangeText`, que entrega directamente el texto. El material destaca `keyboardType`, `autoCapitalize`, `autoComplete`, `secureTextEntry`, `returnKeyType` y `onSubmitEditing`. Para el comportamiento de envío utiliza `submitBehavior` en lugar del antiguo `blurOnSubmit`. **Fuente: Interfaz, p. 7.**

```tsx
<TextInput value={texto} onChangeText={setTexto} placeholder="Escribí algo" />
```

**Fuente: Interfaz, p. 7.**

#### Recorrido de un campo controlado

La práctica construye un campo con etiqueta, placeholder, bordes y estilos, y utiliza `keyboardType` y `autoCapitalize`. Un teclado de correo facilita escribir caracteres habituales, pero **no valida por sí solo la dirección de email**. **Fuente: Clase 03/09/2026, 34:50–57:33.**

El recorrido es **estado → `value` → cambio → setter → nuevo renderizado**. `useState` devuelve el valor conservado por React y una función para solicitar su actualización. Si se pasa un `value` fijo y no se lo actualiza, el campo controlado no refleja lo que se intenta escribir. El mismo estado puede mostrarse en otro `Text`, lo que permite observar que ambos controles dependen del mismo dato. **Fuente: Clase 03/09/2026, 34:50–57:33.**

`onChange` recibe un evento; `onChangeText` recibe directamente el texto. Por eso `onChangeText={setEmail}` pasa la función de actualización sin necesitar un manejador que solo la reenvíe. **Aclaración editorial:** modificar una variable local no solicita un renderizado. Actualizar estado puede provocar una nueva ejecución del componente; no significa «refrescar toda la pantalla» indiscriminadamente. No hace falta `useEffect` para controlar este campo. **Fuentes: Clase 03/09/2026, 34:50–57:33; React, pp. 16 y 22, documentadas en Unidad 2.**

`Pressable` detecta toque y pulsación prolongada. Sus props `style` y `children` pueden ser funciones de `{ pressed }`; permiten presentar feedback sin agregar un estado propio solo para indicar que se está pulsando. **Fuente: Interfaz, p. 8.**

```tsx
<Pressable
  onPress={agregar}
  onLongPress={mostrarOpciones}
  hitSlop={10}
  android_ripple={{ color: "#DDD" }}
  style={({ pressed }) => [e.boton, pressed && e.botonTocado]}
>
  {({ pressed }) => <Text>{pressed ? "Agregando…" : "Agregar"}</Text>}
</Pressable>
```

**Fuente: Interfaz, p. 8.** Las funciones y estilos son auxiliares del ejemplo.

La clase agrega **`TouchableOpacity`** como alternativa que ofrece feedback de opacidad. Esto complementa la recomendación del PDF de utilizar `Pressable`: no implica que la alternativa no exista. Con `Pressable`, el parámetro `pressed` permite cambiar estilos durante el toque; en un arreglo, las propiedades posteriores sobrescriben las anteriores. El estado visual de presionado es distinto del estado persistente usado para decidir si se muestra la contraseña. **Fuente: Clase 03/09/2026, 57:42–1:17:06; contraste: Interfaz, pp. 8 y 26.**

## 2. Bordes, desplazamiento y listas

### Safe area y edge-to-edge

La presentación explica que el contenido puede dibujarse debajo de las barras del sistema. Los insets evitan que reloj, cámara o barra de navegación se superpongan con controles. Propone `react-native-safe-area-context`, usando `SafeAreaView` con `edges` o `useSafeAreaInsets()` para aplicar el espacio en un punto específico, como el final de una lista. **Fuente: Interfaz, pp. 9–10.**

```tsx
import { SafeAreaView } from "react-native-safe-area-context";

<SafeAreaView style={{ flex: 1 }} edges={["top", "bottom"]}>
  <Text>Contenido</Text>
</SafeAreaView>;
```

**Fuente: Interfaz, p. 10.** El material distingue este import del componente homónimo de `react-native`.

La práctica muestra el problema de controles que quedan debajo de barras del sistema o zonas particulares del dispositivo. Se elige dónde aplicar los espacios según la pantalla y la navegación, utilizando `SafeAreaView` o los valores de `useSafeAreaInsets`, en lugar de resolverlo con un margen superior fijo. Los valores observados pertenecen al dispositivo de la demostración y **no son constantes para copiar**. **Fuente: Clase 03/09/2026, 1:17:24–1:23:09.**

`SafeAreaProvider`, cuando corresponde en la estructura de la app, proporciona el contexto de medidas que consumen esos componentes y hooks. Esto no exige agregar un proveedor duplicado en cada pantalla ni demuestra que toda pantalla deba aplicar el mismo espacio en los mismos lados. Las referencias a versiones pertenecen al contexto de la clase. **Fuente: Clase 03/09/2026, 1:17:24–1:23:09, según los aportes recibidos.**

### Qué contenedor utilizar

| Componente    | Problema que resuelve                                               | Límite o característica                                       |
| ------------- | ------------------------------------------------------------------- | ------------------------------------------------------------- |
| `ScrollView`  | Contenido variado de cantidad conocida, formulario o detalle largo. | Crea todos sus hijos aunque no estén visibles.                |
| `FlatList`    | Colección que puede crecer.                                         | Virtualiza filas; ofrece estado vacío, paginación y refresco. |
| `SectionList` | Colección dividida en grupos.                                       | Virtualiza y agrega encabezados de sección.                   |

**Fuente: Interfaz, pp. 11–13.**

#### Películas con `ScrollView` y `map`

Una `View` no vuelve desplazable el contenido que desborda. La clase utiliza `ScrollView` en orientación vertical y horizontal y trata sus indicadores de desplazamiento; las opciones no detalladas en el listado recibido no se reconstruyen. Para contenido pequeño y conocido puede ser suficiente: su límite relevante es que crea todos los hijos, no que toda colección esté prohibida en él. **Fuente: Clase 03/09/2026, 1:23:22–1:39:05.**

El ejemplo usa películas simuladas con título, valoración y color, representadas por componentes con props tipadas. `map` transforma cada dato en un elemento de interfaz; el modelo de película describe los datos y las props describen lo que recibe el componente. Pueden relacionarse sin ser necesariamente la misma interfaz. **Fuente: Clase 03/09/2026, 1:23:22–1:39:05.**

La advertencia de claves repetidas aparece al usar títulos que se repiten. La identidad debe ser única y estable: ni un título repetido ni una posición cambiante son una identidad apropiada para datos que se agregan, eliminan o reordenan. **Fuente: Clase 03/09/2026, 1:23:22–1:39:05; contraste: React, p. 17, documentada en Unidad 2.**

```tsx
<FlatList
  data={productos}
  keyExtractor={(item) => item.id}
  renderItem={({ item }) => <Tarjeta producto={item} />}
  ListEmptyComponent={<Vacio />}
  onEndReached={cargarMas}
  refreshControl={<RefreshControl refreshing={cargando} onRefresh={recargar} />}
/>
```

**Fuente: Interfaz, p. 12.** Es el ejemplo de pull-to-refresh y carga incremental del material. **Aclaración editorial:** presupone un `id` de tipo texto para `keyExtractor`; si el dato usa identificadores numéricos, el fragmento necesita adaptarse. La presentación también advierte que anidar una lista vertical en un `ScrollView` vertical perjudica su virtualización.

#### Ventana de renderizado y tipado de `FlatList`

La clase reemplaza la creación de todos los hijos por una lista virtualizada. Esta mantiene una **ventana de elementos alrededor del área visible**, no solamente lo estrictamente visible. Salir de la ventana de renderizado no equivale a que el dato de la película desaparezca del arreglo en memoria. **Fuente: Clase 03/09/2026, 1:39:08–1:53:32 y 1:54:36–1:55:07.**

`data` contiene los datos y `renderItem` recibe información de cada fila: **`item`, `index` y `separators`**. El tipo de `item` se relaciona con el tipo de elementos del arreglo y con los genéricos de la lista, evitando perder sus comprobaciones de props. `keyExtractor` produce la clave a partir del identificador estable. El índice se usa como salida provisional en la demostración; no se adopta como recomendación para listas que cambian de orden. **Fuente: Clase 03/09/2026, 1:39:08–1:53:32.**

#### Encabezados, refresco y agregado de datos

El recorrido incluye lista horizontal, encabezado con `ListHeaderComponent`, encabezado fijo, pie y `ListEmptyComponent`. Un encabezado incorporado al contenido y uno que se mantiene fijo tienen comportamientos distintos; el listado recibido no permite reconstruir todas las opciones de fijación mostradas. **Fuente: Clase 03/09/2026, 1:39:08–1:53:32.**

Con `RefreshControl`, `refreshing` representa si la operación está en curso y `onRefresh` inicia la acción. La recarga de la clase es **simulada y no está conectada a una API real**. El arreglo de películas se mantiene en estado y se muestra el agregado de elementos; no se deduce de ello un servicio remoto ni un algoritmo de sincronización. **Fuente: Clase 03/09/2026, 1:39:08–1:53:32.**

`onEndReached` permite solicitar más datos al aproximarse al final. **Virtualización y paginación son distintas:** la primera limita el trabajo de renderizar la colección ya disponible; la segunda obtiene o agrega más datos por partes. El ejemplo no demuestra que una API esté implementada. **Fuente: Clase 03/09/2026, 1:39:08–1:53:32 y 1:54:36–1:55:07.**

**Imprecisión oral identificada:** `onEndReachedThreshold` no debe interpretarse como una cantidad de ítems. No se incluye un ejemplo numérico ni se reconstruye una configuración desde esa explicación; la definición precisa y un valor concreto deben verificarse antes de usarlos. `SectionList` se menciona, pero no se desarrolla en la práctica: su explicación anterior conserva la referencia al PDF. **Fuentes: Clase 03/09/2026, 1:39:08–1:53:32; Interfaz, p. 13.**

## 3. Imágenes y formularios

### Imágenes

Se utiliza `Image` de `expo-image`. `source` indica el recurso, `style` el espacio y `contentFit` cómo acomodarlo: `cover` llena recortando y `contain` conserva la imagen completa dejando espacio. El ejemplo agrega una transición de 200 ms. **Fuente: Interfaz, p. 14.**

La tabla de la p. 15 agrega `contentPosition`, placeholder con blurhash o thumbhash, políticas de caché, prioridad, `recyclingKey` para filas recicladas, tinte, desenfoque y texto alternativo. El principio práctico es definir el espacio visual y una estrategia de carga; no asumir que el recurso remoto aparecerá y reservará lugar automáticamente. **Fuente: Interfaz, pp. 14–15.**

El video 4 amplía el ejemplo de **`expo-image`** combinando ajuste de la imagen, placeholder durante la carga, transición al mostrarse y elección de caché en memoria o disco. El ajuste determina cómo ocupa el cuadro —por ejemplo, recortar para cubrir o conservar la imagen completa—; placeholder y transición organizan lo que ve el usuario mientras llega el recurso y cuando aparece. **Fuentes: Clase 17/09/2026, 02:30–11:00; Interfaz, pp. 14–15.**

**Caché y datos de negocio no son equivalentes.** La consulta del PRD permite distinguir una imagen conservada para reutilizar su carga de una lectura, nota u otra operación generada sin conexión que todavía debe sincronizarse. Esa operación necesita un tratamiento local y de envío acorde con el requisito del proyecto; una política de caché de imágenes no resuelve ese circuito. No se asigna a la caché un plazo fijo de conservación ni se la presenta como garantía de que todo recurso estará disponible sin red. **Fuente: Clase 17/09/2026, 02:30–11:00; relación con las orientaciones de diseño de 1:46:20–1:59:21.**

### Formularios controlados

La interfaz no se organiza alrededor de un `<form>` HTML: cada campo se conecta con estado y un botón llama al manejador. El ejemplo de ingreso mantiene `email` y `clave`, utiliza teclado de correo y `autoCapitalize="none"`, y oculta la clave con `secureTextEntry`. **Fuente: Interfaz, p. 16.**

#### Contraseña y control de visibilidad

La clase agrega un estado independiente para la clave y un booleano que permite mostrarla u ocultarla. El campo y el control lateral se agrupan en una `View` con `flexDirection: 'row'`; `Pressable` cambia el booleano y un ternario elige el texto del control. **Fuente: Clase 03/09/2026, 57:42–1:17:06.**

```tsx
import { useState } from 'react';
import { View, Text, TextInput, Pressable } from 'react-native';

export function IngresoDemo() {
  const [email, setEmail] = useState('');
  const [clave, setClave] = useState('');
  const [mostrarClave, setMostrarClave] = useState(false);

  return (
    <View>
      <Text>Correo</Text>
      <TextInput
        value={email}
        onChangeText={setEmail}
        placeholder="tu@email.com"
        keyboardType="email-address"
        autoCapitalize="none"
      />
      <Text>Correo ingresado: {email}</Text>
      <Text>Contraseña</Text>
      <View style={{ flexDirection: 'row' }}>
        <TextInput
          style={{ flex: 1 }}
          value={clave}
          onChangeText={setClave}
          secureTextEntry={!mostrarClave}
        />
        <Pressable onPress={() => setMostrarClave(actual => !actual)}>
          <Text>{mostrarClave ? 'Ocultar' : 'Mostrar'}</Text>
        </Pressable>
      </View>
    </View>
  );
}
```

**Reconstrucción didáctica basada en la explicación oral**, no copia exacta de pantalla. Combina el campo controlado del tramo 34:50–57:33 con la visibilidad de contraseña de 57:42–1:17:06; nombres y distribución mínima se eligen para mostrar el flujo. Cuando `mostrarClave` es verdadero, `secureTextEntry` es falso. No se reproduce la impresión de la contraseña en otro texto o en logs.

Ocultar visualmente el campo **no cifra su valor**. El ejemplo es una interfaz de ingreso, no una implementación de autenticación, validación de credenciales ni almacenamiento seguro. **Fuente: Clase 03/09/2026, 57:42–1:17:06.**

`returnKeyType` cambia la presentación de la tecla; enviar, buscar o pasar al siguiente campo requiere un manejador y la lógica correspondiente. La clase introduce también `multiline`; no se lo convierte en una combinación obligatoria con el campo de contraseña. **Fuente: Clase 03/09/2026, 57:42–1:17:06; contraste: Interfaz, p. 7.**

La validación manual construye un objeto de errores, comprueba que el correo contenga `@` y que la clave tenga al menos ocho caracteres, muestra mensajes y evita enviar si hay errores. La clase lo presenta como suficiente para pocos campos, pero repetitivo cuando crecen reglas y controles. **Fuente: Interfaz, p. 17.**

#### Del control de campos completos a la validación manual

En el video 3 bastaba con que email y contraseña tuvieran contenido para habilitar el paso al listado. El video 4 agrega **comprobación del correo y de la longitud de la contraseña**, construye un objeto de errores y muestra **cada mensaje debajo del campo correspondiente**. Esto permite explicar al usuario qué debe corregir en lugar de tratar el formulario como una única condición sin detalles. **Fuente: Clase 17/09/2026, 12:26–26:44.**

Los mínimos de longitud varían entre ejemplos: se registran como **reglas de las demostraciones**, no como una política universal o un requisito nuevo para todos los grupos. El valor de ocho del párrafo anterior sigue atribuido al PDF. Validar forma y longitud tampoco demuestra que las credenciales sean correctas: **la comprobación mediante API y el acceso con mecanismos del teléfono quedan para otra etapa**. Si el proyecto incluye registro de usuarios, se determina desde el PRD de cada grupo. **Fuente: Clase 17/09/2026, 12:26–26:44.**

#### El mismo formulario con React Hook Form y Zod

Para centralizar las reglas, el PDF propone React Hook Form con Zod:

```tsx
const esquema = z.object({
  email: z.email({ error: "Email inválido" }),
  clave: z.string().min(8, { error: "Mínimo 8 caracteres" }),
});

const {
  control,
  handleSubmit,
  formState: { errors },
} = useForm({ resolver: zodResolver(esquema) });
```

`Controller` conecta cada campo con `value` y `onChange`, `errors` expone los mensajes y `handleSubmit(ingresar)` coordina la validación y el envío. **Fuente: Interfaz, p. 18.** El fragmento presupone los imports de `zod`, `react-hook-form` y `@hookform/resolvers/zod` mostrados en la fuente.

La clase recorre el mismo problema de validación con esas herramientas. Las responsabilidades se encadenan así:

1. **Zod define el esquema** con las reglas de correo y contraseña.
2. **`zodResolver` conecta ese esquema con `useForm`**, para que el formulario utilice sus resultados de validación.
3. **`defaultValues` establece los valores iniciales de los campos**. Evita dejar implícito de dónde parte el formulario; no sustituye las reglas del esquema.
4. **`Controller` vincula cada `TextInput` con su campo**: `value` recibe el valor administrado por el formulario y `onChangeText` llama al `onChange` que proporciona el controlador.
5. **`formState.errors` permite mostrar el mensaje de cada campo** junto a su entrada.
6. **`handleSubmit` se utiliza para ejecutar la función de ingreso cuando las reglas pasan**. Se conecta al control de envío, en lugar de navegar sin comprobar el formulario.

**Fuente: Clase 17/09/2026, 26:44–58:51, según los aportes recibidos.** El ejemplo del PDF anterior conserva su origen: no se presenta como copia exacta de la implementación de clase ni se agregan contratos de API.

**Validez global y error de campo son niveles distintos:** `isValid` informa la validez global del formulario; `errors.email` o `errors.clave` permiten tratar el problema de una entrada concreta. Un único booleano no reemplaza los mensajes que explican qué corregir. **Fuente: Clase 17/09/2026, 26:44–58:51.**

La demostración explora cuándo aparecen errores al **editar, salir del campo o enviar**, pero **no deja fijada una configuración definitiva de ese comportamiento**. Por eso no se reconstruye un `mode` o una política de revalidación como si hubiera quedado acordada. Tampoco se afirma que `handleSubmit` autentique por sí solo al usuario: coordina la validación y la llamada al manejador. **Fuente: Clase 17/09/2026, 26:44–58:51.**

**Aclaración editorial:** la p. 17 utiliza objetos `{}` sin definir el tipo de sus propiedades. Es una simplificación del ejemplo y no una configuración TypeScript completa.

### Teclado

`KeyboardAvoidingView` permite ajustar el contenido para que el teclado no tape los campos. El ejemplo usa `padding` en iOS y `height` en Android. Se menciona `react-native-keyboard-controller` para control más fino y animaciones coordinadas. **Fuente: Interfaz, p. 19.**

En el video 4 el problema se ve en el formulario: al aparecer el teclado, puede tapar el campo activo. `KeyboardAvoidingView` se relaciona con ese ajuste de espacio y disposición, no con validar el dato ni cambiar las reglas del formulario. El comportamiento mostrado conserva el contexto del dispositivo de la práctica. **Fuente: Clase 17/09/2026, 58:51–1:07:58.**

## 4. Estilos, temas y adaptación

Los estilos pueden escribirse en línea o mediante `StyleSheet.create`, normalmente fuera del componente. Los arreglos combinan estilos de izquierda a derecha; los posteriores sobrescriben propiedades y los valores falsos se ignoran. **Fuente: Interfaz, pp. 24 y 26.**

```tsx
<Pressable style={[e.chip, activo && e.chipActivo]}>
  <Text style={[e.texto, activo && e.textoActivo]}>{etiqueta}</Text>
</Pressable>
```

**Fuente: Interfaz, p. 26, fragmento del chip seleccionable.**

Respecto de CSS, la clase destaca nombres de propiedades en objetos, números sin `px`, Flexbox con dirección `column`, propiedades separadas en lugar de atajos como `border: 1px solid red` y ausencia de cascada general. El texto anidado es la excepción de herencia que presenta. **Fuente: Interfaz, p. 25.**

### Input base, estados visuales y botón reutilizable

El ejemplo del video 4 combina **un estilo base del input** con variantes de borde redondeado o de error. El arreglo permite expresar esas diferencias sin copiar todas las propiedades: **si una propiedad se repite, prevalece la del último estilo aplicable**. Así puede mantenerse el mismo tamaño o espaciado y variar el borde según el estado de validación. **Fuentes: Clase 17/09/2026, aproximadamente 1:07:58–1:39:30; Interfaz, pp. 24–26.**

También se extrae un **`AppButton` reutilizable** para compartir la presentación y el comportamiento común del botón, en lugar de repetirlos en cada pantalla. El listado recibido no especifica su interfaz completa ni el archivo exacto: se conserva el propósito de la extracción sin reconstruir props o código de pantalla ausentes. **Fuente: Clase 17/09/2026, aproximadamente 1:07:58–1:39:30.**

### Tema y Context

`useColorScheme()` informa el esquema del sistema. El ejemplo define paletas clara y oscura con fondo, texto y acento, elige una y la aplica. Para evitar repetir esa selección en cada pantalla, propone exponer el tema mediante Context y un hook `useTema()`. **Fuente: Interfaz, p. 28.**

Context permite compartir un valor con descendientes sin pasarlo manualmente por cada nivel. La Unidad 2 disponible incluye `createContext`, un proveedor y `useContext` para un tema. Esta base de los PDF se amplía con la práctica del 01/10 que se integra a continuación. **Fuentes: Interfaz, p. 28; U02 — TypeScript, React y ciclo de vida, p. 24.**

**Fuente pendiente:** el inventario menciona «Context en React: compartir datos con todo el árbol». No se dispone de ese texto en las fuentes locales; esta explicación no sustituye ni presupone su contenido.

La clase trabaja **paletas clara y oscura** y `useColorScheme` para adaptar los colores. Context aparece como **propuesta para compartir el tema con los descendientes de un proveedor**; su implementación manual queda para después. No se registra como una implementación completada en el video 4 y se mantiene aparte el texto independiente de Context. **Fuente: Clase 17/09/2026, aproximadamente 1:07:58–1:39:30.**

#### De Ajustes a un tema compartido

La práctica del 01/10 parte de un **interruptor en Ajustes** que cambia el tema. El encabezado y una tarjeta también necesitan leerlo. Si el valor y el callback se pasan por props, los componentes intermedios deben recibirlos y reenviarlos aunque no los utilicen. El ejemplo muestra cómo esa cadena complica compartir una misma preferencia. **Fuente: Clase 01/10/2026, aproximadamente 15:23–27:48.**

Con Context, un **proveedor expone el valor a sus descendientes** y cada pantalla o componente que lo necesita lo consume. La ubicación del proveedor delimita su alcance: una pantalla fuera de esa parte del árbol no recibe el valor de ese proveedor. Esto reduce el paso manual de props, pero **no garantiza que solamente los consumidores puedan renderizarse**; tampoco es una promesa de optimización general del árbol. **Fuente: Clase 01/10/2026, aproximadamente 15:23–27:48; precisión editorial sobre el alcance del mecanismo.**

#### Construir el proveedor y envolver las pantallas

El recorrido de la demostración consiste en:

1. Crear el contexto con **`createContext`**.
2. Definir un **proveedor que recibe `children`**.
3. Mantener el tema activo mediante **`useState`**.
4. Exponer **tema y función de actualización** en **`value`**.
5. Envolver desde el **layout de Expo Router** las pantallas que compartirán ese estado.
6. Leer el contexto en una pantalla con **`useContext`** o con un **hook propio** que encapsula esa lectura.

**Fuente: Clase 01/10/2026, aproximadamente 31:56–49:11.** Ajustes actualiza el mismo estado que consumen el encabezado y la tarjeta; no se crean copias independientes del tema en cada componente.

El siguiente código es una **reconstrucción didáctica basada en la explicación oral**, no una copia exacta de pantalla. Los nombres y tipos auxiliares se eligen para reunir el proveedor, el tipado y la comprobación del hook de los tramos 31:56–1:06:30:

```tsx
import {
  createContext, useContext, useState,
  type ReactNode, type Dispatch, type SetStateAction,
} from 'react';
import { useColorScheme } from 'react-native';

type Tema = 'claro' | 'oscuro';
type ValorTema = {
  tema: Tema;
  setTema: Dispatch<SetStateAction<Tema>>;
};

const TemaContext = createContext<ValorTema | undefined>(undefined);

export function TemaProvider({ children }: { children: ReactNode }) {
  const esquema = useColorScheme();
  const [tema, setTema] = useState<Tema>(
    () => esquema === 'dark' ? 'oscuro' : 'claro',
  );

  return (
    <TemaContext.Provider value={{ tema, setTema }}>
      {children}
    </TemaContext.Provider>
  );
}

export function useTema() {
  const valor = useContext(TemaContext);
  if (valor === undefined) {
    throw new Error('useTema debe utilizarse dentro de TemaProvider');
  }
  return valor;
}
```

En el layout, el proveedor **envuelve al navegador o al `Slot` que representa las pantallas hijas**. No lo sustituye: devolver solamente el proveedor sin contenido de rutas no muestra por sí solo esas pantallas. Un consumidor puede obtener `const { tema, setTema } = useTema()` y el interruptor solicitar el cambio con `setTema`. **Fuentes: Clase 01/10/2026, aproximadamente 31:56–49:11; relación con la sección 7 de estos apuntes.**

#### Tipado, paleta y comprobación visual

La clase tipa las alternativas **claro/oscuro**, utiliza el esquema del sistema como **valor inicial** y selecciona la paleta según el tema activo. En la reconstrucción anterior, el esquema inicial se traduce una vez al estado; eso no implementa por sí solo una sincronización posterior con cada cambio del sistema. La preferencia se mantiene **durante la ejecución**, mientras que guardarla entre aperturas se menciona como trabajo posterior. **Fuente: Clase 01/10/2026, aproximadamente 49:11–1:06:30.**

El hook propio comprueba que haya proveedor y devuelve un error descriptivo cuando falta. Compartir el tema permite que los componentes reutilizables lean una paleta común sin repetir toda la selección. Sin embargo, la prueba visual detecta otro problema: **un fondo fijo seguía tapando el color de la paleta por el orden de los estilos**. Si ese fondo se aplica después, sobrescribe la misma propiedad; actualizar el estado correctamente no corrige una precedencia de estilos equivocada. **Fuentes: Clase 01/10/2026, aproximadamente 49:11–1:06:30; Interfaz, pp. 24–26.**

#### Paleta derivada y alcance del estado

La paleta se puede **obtener a partir del tema**, sin mantener un segundo estado que haya que sincronizar manualmente. Con tema y paleta en estados separados podrían existir combinaciones incoherentes. El video muestra **`useMemo` para recalcular el valor cuando cambia su dependencia**; se registra como optimización del ejemplo, no como condición para que Context funcione. **Fuente: Clase 01/10/2026, aproximadamente 1:10:02–1:20:09; contraste: React, pp. 16 y 26, documentadas en Unidad 2.**

Como expresión conceptual, `useMemo(() => paletas[tema], [tema])` selecciona la paleta por el tema activo; `paletas` representa las definiciones clara y oscura ya tratadas. Esta expresión es ilustrativa, no una transcripción literal ni un nuevo conjunto de colores. La decisión principal es que la paleta sea **valor derivado**, con o sin memorización, en lugar de otro estado duplicado.

El criterio de diseño distingue **tema, idioma o sesión**, que pueden compartirse, de **datos de un formulario usado por una sola pantalla**, que pueden permanecer locales. No todo estado debe subir al proveedor raíz. **Zustand aparece en una consulta y no se implementa** en esta clase; no se agrega aquí otra solución para repetir el mismo ejemplo. **Fuente: Clase 01/10/2026, aproximadamente 1:10:02–1:20:09.**

#### Consumir fuera del proveedor: comprobación final

El repaso prueba el hook **fuera del proveedor** y observa el error. Es una comprobación del alcance del árbol, no un fallo que se solucione ocultando el mensaje: hay que ubicar al consumidor dentro del proveedor que debe compartir el valor. La prueba explica por qué importa dónde se envuelven las pantallas desde el layout. **Fuente: Clase 01/10/2026, 1:22:36–1:28:27.**

Recuperar una sesión desde almacenamiento local se plantea como **aplicación futura** de ese esquema de proveedor y estado. No se registra como recuperación implementada ni se equipara la preferencia de tema en memoria con una sesión persistida. **Fuente: Clase 01/10/2026, 1:22:36–1:28:27.**

### Diseño responsivo

`useWindowDimensions()` permite reaccionar al cambio de tamaño u orientación. La grilla del material usa tres columnas desde 768, dos desde 576 y una por debajo; cambia `key={columnas}` para remontar la lista cuando cambia la cantidad de columnas. **Fuente: Interfaz, p. 29.**

El video 4 vincula este hook con **cambiar las columnas de una `FlatList` al rotar el dispositivo**. Se adapta la disposición al espacio disponible, sin asumir que todas las pantallas tienen el mismo ancho. Los umbrales numéricos anteriores siguen siendo ejemplos del PDF, no valores universales fijados por la demostración. Las alternativas de estilos y efectos visuales se consultan en el cuadro y apartados existentes, evitando repetir sus definiciones. **Fuente: Clase 17/09/2026, aproximadamente 1:07:58–1:39:30.**

### Alternativas de estilos del material

| Alternativa                        | Propuesta                                                          | Consideraciones de la clase                                               |
| ---------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| StyleSheet + Context + dimensiones | Base sin un sistema adicional.                                     | Válida para proyectos pequeños y para permanecer en Expo Go.              |
| Unistyles                          | Temas, breakpoints y variantes sobre una API similar a StyleSheet. | Opcional; requiere preparación nativa y development build.                |
| NativeWind                         | Clases utilitarias de Tailwind en `className`.                     | Opcional; la presentación lo ubica como compatible con Expo Go.           |
| Tamagui                            | Sistema de diseño con componentes y compilador.                    | Más decisiones y estructura propias.                                      |
| Styled Components                  | CSS-in-JS con template literals.                                   | Se presenta para reconocer código heredado, aunque figura en el programa. |

**Fuente: Interfaz, pp. 27 y 30–32.** Se conservan las decisiones didácticas del PDF sin convertirlas en una recomendación actual verificada para cualquier versión.

## 5. Controles nativos, gestos y animaciones

El material presenta `@expo/ui` para controles de SwiftUI y Jetpack Compose. El ejemplo utiliza `Host`, `Column`, `Switch`, `Picker` y `Button`. `Host` necesita su espacio y el layout interior no es el Flexbox habitual. Los módulos específicos de plataforma pueden cambiar nombres, props y tipos de valores: el selector de fecha de iOS no tiene la misma API que el de Android. **Fuente: Interfaz, pp. 20–22.**

El recorrido del video 4 por **`@expo/ui` y `Host`** es una presentación de controles disponibles: **SwiftUI para iOS y Jetpack Compose para Android**. Se registra con ese alcance, sin suponer que haya reemplazado todos los controles de la aplicación ni completado una integración propia por plataforma. **Fuente: Clase 17/09/2026, 58:51–1:07:58.**

También se menciona `expo-glass-effect` como efecto específico de iOS y se muestra una alternativa con `View` cuando no está disponible. La idea de diseño es que la pantalla conserve su utilidad sin el efecto. **Fuente: Interfaz, p. 33.**

Para gestos se utiliza `react-native-gesture-handler`: el ejemplo de `Gesture.Pan().onUpdate(...)` actualiza las coordenadas de arrastre. Se pueden componer gestos simultáneos, en carrera o excluyentes. Reanimated utiliza valores compartidos y estilos animados para mover trabajo al hilo de UI. **Fuente: Interfaz, pp. 35–36.**

```tsx
const escala = useSharedValue(1);
const estilo = useAnimatedStyle(() => ({
  transform: [{ scale: escala.value }],
}));

<Pressable
  onPress={() => {
    escala.value = withSpring(1.2);
  }}
>
  <Animated.View style={estilo} />
</Pressable>;
```

**Fuente: Interfaz, p. 36.** Cambiar el valor compartido no equivale a actualizar estado de React; la animación no requiere renderizar el componente en cada cuadro.

El video 4 presenta **arrastre y animaciones** como ejemplos. Complementan la explicación de gestos y valores animados del PDF; no se infiere un componente completo ni se copia código no incluido en los aportes recibidos. **Fuente: Clase 17/09/2026, aproximadamente 1:39:30–1:46:20.**

## 6. Accesibilidad

La interfaz debe poder describirse al sistema, utilizarse con VoiceOver o TalkBack y adaptarse a tipografía y preferencias del usuario. La accesibilidad se incorpora al construir los componentes y también ayuda a probarlos por rol y etiqueta. **Fuente: Interfaz, p. 38.**

- `role` describe qué es el control; `accessibilityLabel`, cómo se llama; `accessibilityHint`, una explicación adicional de su acción. **Interfaz, p. 39.**
- `accessibilityState` comunica selección, deshabilitación o estado marcado; `accessibilityValue` describe valores ajustables; las regiones vivas comunican cambios sin mover el foco. **Interfaz, p. 40.**
- Un ícono sin nombre accesible es ambiguo; una imagen decorativa no debe interrumpir la lectura; agrupar toda una pantalla como un elemento impide explorar sus controles. **Interfaz, p. 41.**

La fuente usa como referencias áreas de toque de 44 pt en iOS y 48 dp en Android, y contraste 4,5:1 para texto normal. Son los valores expuestos en el PDF, no una evaluación de conformidad realizada sobre una aplicación. Propone probar el recorrido principal con un lector de pantalla y verificar también en dispositivos reales. **Fuente: Interfaz, pp. 41–42.**

La práctica sugerida en clase es **elegir una pantalla del integrador**, identificar sus controles mediante **roles y etiquetas** y probar el recorrido con **TalkBack en Android o VoiceOver en iOS**. El rol indica **qué tipo de control es**; la etiqueta le da **un nombre**. Se evalúa así si una persona puede reconocer y utilizar la pantalla, no solo si los controles tienen una apariencia adecuada. **Fuente: Clase 17/09/2026, aproximadamente 1:39:30–1:46:20.**

## 7. Expo Router: archivos que definen rutas

La navegación debe resolver cambios de pantalla, historial, botón atrás y apertura desde enlaces. React Navigation registra pantallas; Expo Router se construye sobre él y las deriva del sistema de archivos. **Fuente: Navegación, pp. 2–3.**

### Punto de entrada: dos proyectos de la demostración

El docente compara una plantilla con **`index.ts` y `App.tsx`** con otra que utiliza **Expo Router**. En la primera explica el papel de `NavigationContainer` al usar React Navigation directamente: contiene el sistema de navegación configurado por la aplicación. No se deduce que cualquier plantilla deba traer ya las mismas pantallas o la misma configuración. **Fuentes: Video 2 — Navegación, 01:08–10:14; Navegación, p. 3.**

En el proyecto con Expo Router, `package.json` utiliza **`expo-router/entry`** como entrada. El docente crea **`app/index.tsx`** y comprueba que aparece la pantalla inicial. El punto de entrada del paquete y el archivo de la ruta cumplen funciones distintas: el primero inicia el mecanismo de Router y el segundo define la pantalla. No se traslada sin cambios el armado manual de `NavigationContainer` al ejemplo de Expo Router. **Fuente: Video 2 — Navegación, 01:08–10:14, según los aportes recibidos.**

**Aclaración editorial:** la demostración usa `app/`, mientras el árbol del PDF que se conserva a continuación usa `src/app/`. Se identifican las estructuras de cada fuente, sin inventar una migración ni afirmar que el proyecto mostrado tenga ambos directorios.

#### Del proyecto vacío al Stack en el video 3

La práctica del 10/09 retoma el punto de entrada del video 2: crear la pantalla inicial, envolverla desde **`_layout.tsx`** e incorporar **`Stack`** para la navegación y su encabezado. Sobre esa estructura se configuran opciones comunes al navegador o particulares de una pantalla. Se vincula así la existencia del archivo de pantalla con el layout que lo presenta, sin repetir la definición de cada tipo de ruta. **Fuente: Clase 10/09/2026, 16:21–49:06; relación con Video 2 — Navegación, 01:08–17:27.**

La consulta sobre **`app/` frente a `src/app/`** se registra como una duda acerca de la estructura del proyecto. No se deduce de ella que una ubicación deba sustituirse automáticamente por la otra. Los comentarios sobre compatibilidad de SDK pertenecen a esa clase y no fijan requisitos actuales verificados. **Fuente: Clase 10/09/2026, 16:21–49:06.**

### Archivos, rutas y contenido de los layouts

```text
src/app/
  _layout.tsx
  index.tsx
  (tabs)/
    perfil.tsx
  producto/
    [id].tsx
  docs/
    [...ruta].tsx
  +not-found.tsx
```

`index.tsx` representa la entrada de una carpeta; `[id]`, un parámetro; `[...ruta]`, el resto del recorrido; `(tabs)`, una agrupación que no agrega un segmento a la URL; `+not-found`, una ruta no encontrada. `_layout.tsx` define cómo envolver y navegar las rutas hijas. **Fuente: Navegación, p. 4.**

En la práctica, **`app/index.tsx`** corresponde a la ruta de entrada y **`detalle.tsx`** a **`/detalle`**. Un segmento **`[id]`** captura un valor dinámico; **`[...ruta]`** captura varios segmentos. La organización del árbol se relaciona con la URL, pero no obliga a registrar manualmente cada pantalla como en el otro proyecto. **Fuente: Video 2 — Navegación, 10:14–17:27.**

El ejemplo que muestra el papel del layout es crear un **`_layout.tsx` que devuelve solamente contenido propio**: la pantalla hija deja de verse aunque `index.tsx` siga existiendo. **El archivo existe, pero el layout no está mostrando la ruta hija.** Para hacerlo, debe incluir el lugar donde se representa esa hija mediante **`Slot`** o un navegador como **`Stack`**, según el comportamiento buscado. **Fuentes: Video 2 — Navegación, 10:14–17:27; Navegación, pp. 8 y 17.**

La carpeta **`(tabs)`** agrupa archivos sin agregar ese nombre a la URL; los paréntesis no crean por sí solos una barra de pestañas. El componente **`Tabs`** del layout es el que configura esa navegación. **Fuentes: Video 2 — Navegación, 10:14–17:27; Navegación, pp. 4 y 14.**

**Dos significados de «ruta» en el caso de la cooperativa:** una **ruta de reparto o de lectura** es el recorrido de suministros que pertenece al problema del negocio; una **ruta de navegación de Expo Router** identifica una pantalla o destino de la aplicación. Seleccionar un recorrido puede llevar a su pantalla de detalle, pero no convierte el recorrido físico en un archivo del router. **Contexto: Clase 10/09/2026, aproximadamente 1:06:00–1:18:01; distinción editorial de los términos utilizados.**

### Stack, Tabs, Drawer y Slot

| Opción              | Uso principal                                                          | Referencia Navegación |
| ------------------- | ---------------------------------------------------------------------- | --------------------- |
| Stack               | Secuencia lista → detalle → editar, con historial.                     | pp. 6–8               |
| Tabs                | Secciones paralelas, cada una con su estado de navegación.             | pp. 13–14             |
| Drawer              | Menú lateral; necesita dependencias y `GestureHandlerRootView`.        | p. 15                 |
| Modal               | Presentación de una pantalla del Stack, por ejemplo filtros o carrito. | pp. 8 y 16            |
| Pestañas superiores | Subdividir una sección; se menciona Material Top Tabs.                 | p. 16                 |
| Slot                | Insertar la ruta hija en un layout sin agregar navegador.              | p. 17                 |

`Stack` conserva pantallas anteriores para volver. `screenOptions` configura el conjunto y `options` particulariza una pantalla. No es necesario registrar en el layout cada ruta para que exista; se nombran las que requieren opciones distintas. **Fuente: Navegación, pp. 7–8.**

#### Stack de películas: ruta y presentación

El ejemplo de películas permite distinguir las opciones compartidas por el navegador, **`screenOptions`**, de las opciones de una **`Stack.Screen`** concreta, **`options`**. Una pantalla puede ajustar su presentación sin repetir toda la configuración común. **Fuentes: Video 2 — Navegación, 17:27–26:46; Navegación, p. 8.**

En esa configuración, **`name` identifica la ruta** y **`title` cambia el texto visible**, por ejemplo el del encabezado. Cambiar el título no equivale a renombrar el archivo ni a crear otra URL. Se conserva la diferencia entre la identidad de la pantalla y su presentación al usuario. **Fuente: Video 2 — Navegación, 17:27–26:46.**

#### Inicio y perfil como pestañas

En el layout del grupo se configura **`Tabs`** y se particularizan las pantallas de **inicio y perfil** con sus títulos e íconos. En términos de las opciones que explica el PDF, `Tabs.Screen` identifica la ruta, `title` proporciona su rótulo y `tabBarIcon` devuelve el componente de ícono. La carpeta agrupa y el navegador convierte esas pantallas en secciones accesibles mediante pestañas. **Fuentes: Video 2 — Navegación, 27:16–32:39; Navegación, pp. 13–14.**

Los intentos de instalación durante la demostración no se convierten en una secuencia obligatoria de preparación. Tampoco se inventan nombres exactos de íconos o dependencias a partir de ese intercambio; las referencias de instalación del PDF conservan su propia atribución y contexto.

En el video 3 se combinan **pestañas y stacks mediante layouts anidados**. El conflicto al repetir nombres de pantalla muestra la necesidad de revisar qué archivos y qué layout corresponden a cada destino; cambiar solo un título visible no resuelve necesariamente una confusión de identidad de rutas. El listado recibido no permite reconstruir los nombres exactos ni una reorganización literal de carpetas. **Fuente: Clase 10/09/2026, aproximadamente 1:06:00–1:18:01.**

En ese mismo recorrido se vuelve a observar que las carpetas entre paréntesis agrupan sin agregar su nombre a la URL. Esto debe considerarse al organizar pantallas: la carpeta no crea por sí sola un segmento visible que diferencie destinos. **Drawer queda como mención**, no como una práctica completa adicional. **Fuente: Clase 10/09/2026, aproximadamente 1:06:00–1:18:01; contraste: Navegación, p. 4.**

Se pueden anidar navegadores, por ejemplo un Stack por pestaña. En el ejemplo del **PDF**, para evitar dos headers se desactiva el superior en la ruta del grupo. `Slot` sirve para un layout de proveedores, pero no aporta por sí mismo historial, transiciones o conservación de la pantalla anterior como un Stack. **Fuente: Navegación, pp. 17–18.**

#### Navegadores anidados y elección del header

En el **video**, el docente coloca un **Stack dentro de la sección de películas** y aparecen dos encabezados: uno del navegador principal y otro del interior. En esa demostración **oculta el interior para conservar el principal**. Se distingue del ejemplo del PDF, que apaga el superior: la decisión depende de cuál encabezado se quiere mantener en esa estructura. **Fuentes: Video 2 — Navegación, 32:39–35:44; Navegación, p. 18.**

Drawer se menciona brevemente como menú lateral. Modal y pestañas superiores se nombran como alternativas; no se presentan como prácticas completas de ese tramo. El desarrollo anterior de sus propósitos sigue atribuido al PDF. **Fuentes: Video 2 — Navegación, 32:39–35:44; Navegación, pp. 15–16.**

### Header

El header pertenece al navegador, no al contenido de la pantalla. Sus opciones controlan título, colores, tipografía, acciones, transparencia y buscador. Una pantalla puede declarar `Stack.Screen` para ajustar el título cuando llegan datos. **Fuente: Navegación, pp. 9–10.**

Si se utiliza `headerShown: false`, deben resolverse el espacio seguro superior, la acción de volver y el título o identificación de la pantalla. Ocultarlo puede tener sentido en pantalla completa, para un diseño propio o al anidar navegadores. **Fuente: Navegación, pp. 11–12.**

La clase muestra que **el header lo dibuja el navegador**, no el componente de contenido de la pantalla. Si se lo oculta para construir uno propio, hay que decidir cómo respetar el área segura y, cuando corresponda, ofrecer una forma de volver. Ocultar un header duplicado en una estructura anidada no implica que siempre haya que reemplazar los dos. **Fuente: Video 2 — Navegación, 17:27–26:46 y 32:39–35:44.**

El video 3 practica la configuración de encabezados tanto para el conjunto como para una pantalla. Al ocultar el header del ingreso se retoma el área segura: quitar la barra del navegador no significa que reloj y demás zonas del sistema dejen de ocupar espacio. Se conserva el criterio de aplicar los insets donde corresponde, en lugar de copiar un margen fijo. **Fuente: Clase 10/09/2026, 16:21–49:06 y aproximadamente 49:06–1:06:00; relación con la sección 2 de estos apuntes.**

### Moverse y pasar datos

```tsx
<Link href="/perfil">Ver perfil</Link>
<Link href={`/producto/${id}`}>Ver producto</Link>

router.push('/perfil');
router.replace('/inicio');
router.back();
router.dismiss();
```

`Link` expresa un enlace; `push` apila; `replace` reemplaza la entrada actual; `back` vuelve; `dismiss` se utiliza en el ejemplo para cerrar una presentación modal. Después de un login, el material propone `replace` para evitar volver al formulario con atrás. **Fuente: Navegación, p. 19.**

En el repaso final, **`Link`** permite navegar con un enlace, **`router.push`** agrega una entrada al historial y **`router.replace`** reemplaza la actual. La diferencia afecta a qué se podrá volver, no solo al aspecto de la nueva pantalla. **Fuente: Video 2 — Navegación, 35:52–37:34.** Los fragmentos anteriores se conservan como ejemplos del PDF, no como transcripción exacta del código de la clase.

#### Del formulario de ingreso al listado

El video 3 conecta el formulario practicado en el video 1 con la navegación del video 2: **email y contraseña en estado → botón deshabilitado mientras falten datos → navegación al listado al presionarlo**. La comprobación de la demostración es que ambos campos tengan contenido. No verifica credenciales contra un servidor ni demuestra que exista una sesión autenticada. **Fuente: Clase 10/09/2026, aproximadamente 49:06–1:06:00.**

Se utiliza **`replace` para salir del ingreso**, reemplazando esa entrada del historial, y **`push` cuando interesa poder volver a la pantalla anterior**, como en un recorrido de listado a detalle. La elección es de comportamiento de navegación, no una prueba de autenticación. El login real queda para más adelante. **Fuente: Clase 10/09/2026, aproximadamente 49:06–1:06:00; contraste: Navegación, p. 19.**

Los parámetros se leen con `useLocalSearchParams`. Pueden formar parte de `/producto/42` o ser query params, como `/buscar?q=zapatillas&orden=precio`. El ejemplo tipa `id` como texto y lo convierte con `Number(id)` antes de tratarlo como número. **Fuente: Navegación, p. 20.**

El video enfatiza esa precaución con el identificador del ejemplo: **`"42"` y `42` no son iguales con `===`**, porque uno es texto y el otro número. Debe distinguirse el parámetro recibido de su uso numérico; no se presupone que el valor ya tenga el tipo de un identificador del modelo. **Fuente: Video 2 — Navegación, 35:52–37:34.**

#### Selección de un recorrido y título del detalle

La práctica del 10/09 desarrolla esta secuencia: **seleccionar una ruta de reparto → navegar con su `id` → leer el parámetro en el detalle → cambiar el título del encabezado mediante `navigation.setOptions`**. El parámetro identifica el recorrido seleccionado; no es necesario transportar en él todo su contenido. **Fuente: Clase 10/09/2026, 1:18:01–1:29:37.**

Este ejemplo complementa la declaración de opciones con `Stack.Screen` del PDF: el método `navigation.setOptions` modifica las opciones del navegador desde la pantalla. Se plantea como uso posterior **consultar una API para obtener el nombre del ítem** y utilizarlo en el encabezado; esa consulta no se da por implementada. **Fuentes: Clase 10/09/2026, 1:18:01–1:29:37; Navegación, pp. 9–10.**

También se prueba una captura **`[...muchos]`**, que recibe varios segmentos como un **arreglo**, en lugar de tratar todo el recorrido como un único `id`. La relación con `[...ruta]` del PDF es el patrón de captura, no una obligación de usar el mismo nombre de archivo. No se inventa una URL concreta ni código literal de esa prueba. **Fuentes: Clase 10/09/2026, 1:18:01–1:29:37; Navegación, p. 4.**

### Protección de rutas

```tsx
<Stack>
  <Stack.Protected guard={!!sesion}>
    <Stack.Screen name="(privado)" />
  </Stack.Protected>
  <Stack.Protected guard={!sesion}>
    <Stack.Screen name="login" />
  </Stack.Protected>
</Stack>
```

La disponibilidad depende del guard. El objetivo del ejemplo es impedir que se muestre brevemente una pantalla privada antes de una redirección. **Fuente: Navegación, p. 21.** **Aclaración editorial:** esto controla navegación en el cliente; no demuestra autorización para acceder a datos de un servidor.

En el video, **`Stack.Protected` y `guard` se presentan como adelanto de autenticación**, no como un login completo ni una autorización del backend implementada. Se conserva la distinción anterior: limitar las rutas disponibles al cliente no sustituye comprobar el acceso a los datos en el servidor. **Fuente: Video 2 — Navegación, 35:52–37:34.**

El video 3 avanza sobre ese adelanto **cambiando un `guard` booleano** para mostrar el ingreso o las pantallas privadas. Es una **sesión simulada**, útil para observar qué rutas se habilitan al cambiar la condición. La persistencia del token, el login completo y la integración con APIs quedan para después; no se consideran resueltos por alternar el booleano. El repositorio se anuncia para una clase posterior, sin que ese anuncio aporte aquí su contenido. **Fuente: Clase 10/09/2026, 1:29:37–1:36:18, final del texto recibido.**

**Límite del cierre:** la transcripción se interrumpe en medio de una frase a **1:36:18**. No se completa la intervención ni se presume el resultado posterior de la demostración. La distinción entre control de rutas del cliente y autorización sobre datos del servidor sigue vigente.

## Cierre audiovisual y fuente escrita pendiente

- Ambos PDF quedaron integrados. La práctica indicada consiste en pantallas con tema claro/oscuro y diseño adaptable. **Interfaz, p. 43.**
- El texto independiente de Context sigue pendiente de incorporación; no se inventa su contenido.
- Las decisiones sobre librerías, APIs y compatibilidad corresponden a las versiones de las fuentes.
- **Estado audiovisual: 5 de 5 videos incorporados.** Se verificaron el 03/09/2026, el video 2 «Navegación» sin fecha informada, el 10/09/2026, el 17/09/2026 y el 01/10/2026. No quedan videos por recibir ni búsquedas audiovisuales abiertas para esta unidad.
- La transcripción automática identificada por el usuario llega a **1:55:20 e incluye la despedida**. Se conserva el límite de integración desde los aportes recibidos; no se inventa un enlace.
- El **video 1** desarrolla componentes, campos y estado, respuesta al toque, áreas seguras y listas; allí navegación, protección de rutas y animaciones solo se anuncian para otras clases.
- El **video 2** amplía entrada del proyecto, rutas, layouts, Stack, headers, pestañas y navegadores anidados. Drawer, modal y pestañas superiores se mencionan; `Stack.Protected` y `guard` quedan como adelanto de autenticación. No se atribuye a ese video un desarrollo de animaciones ni de autorización de datos. Los desarrollos de los PDF se conservan con sus referencias.
- El **video 3** vincula el PRD de la cooperativa y sus maquetas con la práctica de Stack, ingreso simulado, listado, pestañas, detalle y guard booleano. Las referencias offline del diseño no prueban que estén implementadas persistencia o sincronización. Login, token y APIs se proyectan para más adelante.
- La transcripción del **10/09/2026** termina a **1:36:18 en medio de una frase**. Se conserva esa limitación y no se inventa enlace ni contenido posterior. El texto independiente de Context permanece como aporte separado pendiente.
- El **video 4** amplía imágenes y caché, validación manual y con React Hook Form/Zod, teclado, controles nativos, estilos reutilizables, temas, diseño adaptable, gestos y accesibilidad. Las consultas de PRD se registran como orientaciones de diseño offline, no como sincronización implementada.
- La transcripción del **17/09/2026** llega a **1:59:21 e incluye la despedida**. No se proporciona enlace. Siguen sin desarrollarse en esta clase la autenticación por API, el acceso mediante mecanismos del teléfono y la implementación manual de Context; APIs, permisos y notificaciones se anuncian para Unidad 4.
- El **video 5 del 01/10/2026** desarrolla la práctica de Context anunciada el 17/09: proveedor, estado compartido, hook, paleta derivada, precedencia de estilos y prueba fuera del proveedor. Llega a **1:28:27 e incluye el cierre**, sin enlace proporcionado. Persistir la preferencia o recuperar la sesión se mencionan como trabajos posteriores; Zustand y push no se implementan.
- **Indicación del 03/09, 1:53:50–1:54:29:** ante la consulta sobre testing, depuración y rendimiento para la entrega, el docente los presenta como teoría que se retomará después. Se registra con esa fecha y alcance, sin eliminar la teoría existente ni generalizarlo a futuras consignas. No se modifica el archivo de Unidad 2.

**Estado de la fuente independiente:** se revisaron los archivos locales y las menciones del inventario; no se encontró el texto **«Context en React: compartir datos con todo el árbol»**. Los aportes del video 5 se atribuyen a esa clase y no al texto ausente. El cierre queda registrado como **«Audiovisuales completos; pendiente la integración del texto independiente de Context»**, sin declarar integrado un material que no se pudo leer.
