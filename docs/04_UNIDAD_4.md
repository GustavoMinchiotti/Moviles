# Unidad 4 — Librerías, permisos y APIs del dispositivo

[Volver al índice](00_INDICE.md)

**Estado: Documentación completa respecto del material disponible. Audiovisuales: 5 de 5 videos incorporados.** Se conservan los tres PDF y se verificaron las incorporaciones de **T01.1, T01.2, T01.3, la clase del 08/10/2026 y T01.4**. No quedan videos por incorporar del listado confirmado. Los cortes de las transcripciones anteriores y el enlace de Drive sin identificar se conservan como limitaciones de las fuentes, sin bloquear el cierre ni contar ese enlace como sexto video.

## Fuentes y alcance

| Referencia | Fuente original | Páginas |
| --- | --- | --- |
| **Permisos** | [U04.01 - Librerías, plugins y permisos.pdf](../fuentes/pdf/U04.01%20-%20Libreri%CC%81as%2C%20plugins%20y%20permisos.pdf) | 26 |
| **APIs** | [U04.T02 - APIs del dispositivo.pdf](../fuentes/pdf/U04.T02%20-%20APIs%20del%20dispositivo.pdf) | 34 |
| **Notificaciones** | [U04.T03 - Notificaciones.pdf](../fuentes/pdf/U04.T03%20-%20Notificaciones.pdf) | 29 |

El programa, p. 3, incluye cámara y selección de imágenes, ubicación y mapas, sensores, hápticos y archivos. Se incorporan multimedia y notificaciones porque los materiales suministrados los presentan en esta unidad. Se cita la página del visor, incluida la portada; en Notificaciones algunas diapositivas continúan en la página siguiente. Las versiones y compatibilidades se documentan según los PDF, sin comprobación externa ni ejecución de comandos.

**Fuente audiovisual:** [U04 - T01.1](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=55985), video 1 de 5; fecha de grabación no indicada. El usuario informa que la transcripción automática termina a **12:22, a mitad de una explicación**. Se registra como **corte del texto**, no como final demostrado de la grabación.

**Segunda fuente audiovisual:** [U04 - T01.2](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=55986), video 2 de 5; fecha no informada. El docente confirma que la grabación anterior se interrumpió. **T01.2 reinicia el contador**: sus marcas no se suman a los 12:22 de T01.1. El texto de T01.2 termina a **11:43, en medio de una frase**; se registra ese límite sin reconstruir su continuación.

**Tercera fuente audiovisual:** [U04 - T01.3](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=55987), video 3 de 5; fecha no informada. Según los datos proporcionados, el reproductor indica **9:23 de duración** y la última marca de la transcripción es **9:16**, con despedida. Se distinguen duración del reproductor y última marca textual; los tiempos de T01.3 son propios de este video. Su enlace tampoco pudo consultarse desde la herramienta disponible: se integran los aportes recibidos, sin atribuir revisión directa ni transcripción literal completa.

**Cuarta fuente audiovisual:** [Clase del 08/10/2026](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=56277), video 4 de 5. La transcripción identificada por el usuario llega a **1:43:00 e incluye la despedida**. El enlace del campus no fue accesible desde la herramienta disponible; se integran los aportes y marcas recibidos, sin atribuir una revisión directa ni reconstruir código literal ausente.

**Quinta fuente audiovisual:** [U04 - T01.4](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=56420), video 5 de 5; fecha de grabación no informada. Duración indicada por el usuario: **1:31:15**. Última marca de transcripción: **1:31:08, con cierre**. Se distinguen ambas referencias temporales. El enlace no fue accesible desde la herramienta disponible: se integran los aportes y tiempos recibidos sin atribuir una revisión directa ni completar código no proporcionado.

**Alcance de la integración:** se utilizan los aportes y marcas de tiempo proporcionados en el pedido, no una revisión directa del video ni el cuerpo literal completo de los subtítulos. El enlace del campus no pudo consultarse desde la herramienta disponible. Los desarrollos posteriores del PDF conservan su atribución; no se presentan como explicaciones completas de este fragmento audiovisual.

La misma limitación de consulta se aplica a T01.2: su enlace del campus no fue accesible desde la herramienta disponible. La integración distingue los aportes recibidos de cada video y la explicación escrita de los PDF.

## 1. De JavaScript al hardware

Una llamada desde JavaScript llega a un módulo nativo escrito en Swift o Kotlin y de allí a una API del sistema. La presentación lo ilustra con cámara, AVFoundation en iOS y CameraX en Android. Agregar una librería nativa cambia el binario; no es solo agregar código JavaScript. **Fuente: Permisos, pp. 4–5.**

Hay dos condiciones independientes: **permiso**, que el usuario autorice, y **disponibilidad**, que el dispositivo tenga la capacidad. Un permiso concedido no crea un sensor ausente y una cámara disponible no autoriza usarla. **Fuente: Permisos, p. 4.**

El video concreta esta diferencia en dos casos que la app debe prever:

- **El usuario deniega la cámara:** puede existir la capacidad, pero la aplicación no está autorizada a utilizarla. Debe tratar ese rechazo en su interfaz y en su flujo.
- **El dispositivo carece de acelerómetro:** pedir permiso no resuelve la ausencia del sensor. Debe contemplarse que la funcionalidad no esté disponible en ese equipo.

La toma de una foto vincula esas condiciones con el recorrido técnico ya explicado: **llamada desde JavaScript/TypeScript → módulo nativo → API de cámara del sistema**, con **AVFoundation en iOS y CameraX en Android**. Tener una función accesible desde el código no elimina la autorización ni la comprobación de disponibilidad que corresponda. **Fuentes: U04 - T01.1, 01:22–03:26, según los aportes recibidos; Permisos, pp. 4–5.**

La clase propone buscar primero en Expo SDK, después en la comunidad —consultando plataforma, mantenimiento y compatibilidad— y, si no existe solución, reconocer la posibilidad de un módulo propio, fuera del alcance de la materia. **Fuente: Permisos, pp. 6–7.**

### Elegir una librería leyendo su ficha

El recorrido del video comienza por **Expo SDK**, pasa a **React Native Directory** para paquetes de terceros y contempla un **módulo propio** cuando las opciones existentes no cubren la necesidad. El objetivo es decidir qué solución se puede incorporar al proyecto, no instalar el primer paquete cuyo nombre parezca adecuado. **Fuente: U04 - T01.1, 03:33–08:35.**

Se utiliza **`expo-clipboard`** como ejemplo de lectura de documentación: es un módulo para trabajar con el **portapapeles**. La ficha se consulta para reconocer su propósito, **plataformas admitidas**, **inclusión en Expo Go**, **instalación** y **API de uso**. Esas preguntas deben acompañarse con revisión de mantenimiento, compatibilidad con el SDK del proyecto y permisos necesarios. **Fuentes: U04 - T01.1, 03:33–08:35; Permisos, pp. 6–8.**

```bash
npx expo install expo-clipboard
```

**Fuente: U04 - T01.1, 03:33–08:35.** Es el comando presentado como ejemplo de instalación. La clase explica la instalación **sin mostrar una prueba de lectura o escritura del portapapeles**. No se inventan llamadas concretas de su API ni resultados de ejecución; tampoco se convierte la lectura de esa ficha en una comprobación actual de plataformas o compatibilidades.

```bash
npx expo install expo-camera
npx expo install --check
```

El instalador de Expo selecciona versiones compatibles con el SDK para los paquetes que conoce; `--check` revisa dependencias. Antes de elegir una librería se verifica plataforma, inclusión en Expo Go, mantenimiento, arquitectura admitida y permisos incorporados. **Fuente: Permisos, pp. 7–8.**

### Expo Go y development build

Permisos enumera cámara, picker, ubicación, sensores, hápticos, archivos, `react-native-maps` y notificaciones locales como capacidades para comenzar en Expo Go. Distingue push en Android desde SDK 53, `expo-maps` y módulos no incluidos como situaciones que requieren un development build. También lo requiere aplicar configuraciones nativas propias. **Fuente: Permisos, p. 9.**

**Aclaración editorial:** esto precisa la mención general de notificaciones de la Unidad 1: la disponibilidad de locales no equivale a poder probar push con cualquier Expo Go.

El docente orienta a **comenzar con módulos incluidos en Expo Go**. La distinción técnica es que instalar un paquete JavaScript en el proyecto **no incorpora código nativo al binario de Expo Go que ya está instalado**. Si la capacidad nativa no está allí, no aparece solo por agregar la dependencia o recargar JavaScript. Un **development build** permite probar una compilación propia con los módulos y la configuración nativa de la aplicación. **Fuente: U04 - T01.1, 08:41–11:02.**

Locales y push se **anticipan** en ese tramo, sin una implementación de notificaciones. Se conservan las precisiones de plataforma y SDK del PDF anterior y de la sección 9: la orientación introductoria del video no las reemplaza ni demuestra que todas las notificaciones funcionen del mismo modo en Expo Go. **Fuentes: U04 - T01.1, 08:41–11:02; Permisos, p. 9.**

## 2. Configuración nativa y config plugins

La **generación nativa continua (CNG)** trata `android/` e `ios/` como artefactos generados desde configuración y plugins. En el flujo de la clase se versiona la configuración y se reconstruyen los directorios, en lugar de mantener cambios manuales dispersos en manifiestos, Gradle o Podfile. **Fuente: Permisos, pp. 11–13.**

El fragmento audiovisual introduce la comparación con tareas que antes se realizaban a mano: **modificar `AndroidManifest.xml` y la configuración de Gradle en Android e instalar pods en iOS**. Ese trabajo sirve como contraste para comprender CNG y la generación de la configuración nativa. **Fuente: U04 - T01.1, 11:02–12:22.**

La transcripción se corta a mitad de esta explicación. Por eso, el desarrollo de **config plugins**, los ejemplos de `app.json`, la recompilación y el flujo de declaración/solicitud de permisos que siguen **mantienen su atribución a los PDF**. No se deduce que el video haya completado esos temas ni se reconstruyen comandos de Gradle o de instalación de pods a partir del anuncio. **Fuentes de la ampliación escrita: Permisos, pp. 12–25.**

### De `app.json` a los proyectos nativos

T01.2 retoma la comparación interrumpida: el docente parte de la configuración Expo, muestra **identificadores e íconos** y ejecuta:

```bash
npx expo prebuild
```

El recorrido muestra la generación de **`android/` e `ios/`** desde esa configuración. Hay que distinguir **generar o actualizar los proyectos nativos**, tarea de `prebuild`, de **compilarlos después para producir un binario**. El comando no equivale por sí solo a completar una build instalable. **Fuente: U04 - T01.2, 00:07–03:59, según los aportes recibidos.**

### Dónde termina la configuración en la demostración

| Plataforma | Archivo o directorio inspeccionado | Papel en el proyecto mostrado |
| --- | --- | --- |
| iOS | `Info.plist` | Configuración y descripciones de uso de capacidades. |
| iOS | `Podfile` y `Pods` | Declaración e instalación de dependencias nativas. |
| Android | `AndroidManifest.xml` | Declaraciones de permisos del proyecto. |
| Android | `build.gradle` | Configuración de compilación y dependencias. |
| Android | `res/` | Íconos de distintas densidades y recursos del splash. |

**Fuente: U04 - T01.2, 03:59–07:45.** Los permisos y recursos inspeccionados corresponden **al proyecto de la demostración**; no se presentan como una lista obligatoria de toda app o de cualquier versión de Expo. El cuadro relaciona configuración y resultado nativo sin inventar rutas absolutas ni valores no recibidos.

Los config plugins son funciones que aplican cambios nativos durante la generación. En `plugins`, un nombre solo usa valores predeterminados y un arreglo `[nombre, opciones]` personaliza el comportamiento:

```json
{
  "expo": {
    "plugins": [
      "expo-router",
      ["expo-camera", {
        "cameraPermission": "Sacamos la foto del producto que vas a publicar.",
        "microphonePermission": "Grabamos la nota de voz que adjuntás.",
        "recordAudioAndroid": true
      }]
    ]
  }
}
```

**Fuente: Permisos, p. 14, extracto de configuración.** Es un ejemplo que incluye audio porque plantea grabación, no una indicación de pedir micrófono en toda app de fotos.

### `expo-camera`: personalizar el módulo

T01.2 muestra el mismo patrón **`[nombre, opciones]`** dentro de `plugins`. En el ejemplo de clase, la descripción de uso de cámara en iOS explica que se utilizará **para leer un código QR**. Se distingue de la foto de producto del ejemplo del PDF anterior: son motivos de uso de sus respectivos proyectos, no textos para copiar indiscriminadamente. También se mencionan micrófono y la opción de grabar audio en Android. **Fuentes: U04 - T01.2, 07:53–09:12; Permisos, p. 14.**

Estas opciones **configuran el binario**. No equivalen a que el usuario ya haya autorizado el acceso: la solicitud cuando la app se ejecuta sigue siendo otro momento, desarrollado con atribución al PDF en la sección 3. **Fuentes: U04 - T01.2, 07:53–09:12; Permisos, pp. 18–23.**

Cambios de componentes, estilos o librerías solo JavaScript se reflejan al recargar. Una librería nativa, un plugin o cambios de permisos, íconos, nombre y esquema de URL requieren regenerar y compilar. La clase muestra `npx expo prebuild --clean` dentro de ese proceso. Recargar no cambia el manifiesto que ya tiene el binario instalado. **Fuente: Permisos, p. 15.**

**Aclaración editorial:** la p. 16 contrapone editar nativo manualmente con CNG. El aspecto relevante es mantener o abandonar la regeneración como fuente de verdad; no se interpreta que abrir una carpeta por sí solo transforme automáticamente el proyecto.

### Recargar o generar y compilar de nuevo

| Cambio | Tratamiento que contrasta el video |
| --- | --- |
| Estilos, estado, navegación o lógica JavaScript, sin una nueva necesidad nativa | Recargar el código del proyecto. |
| Código nativo que no existe en el binario instalado | Generar y compilar una versión que lo incluya. |
| Permisos, plugins o íconos que cambian la configuración nativa | Incorporar el cambio a los proyectos nativos y compilar una nueva versión. |

**Fuente: U04 - T01.2, 09:12–11:28.** El caso del **módulo que sigue sin aparecer después de recargar** sirve para localizar el límite: la recarga no agrega al binario código nativo que no estaba compilado. No se resuelve repitiendo la recarga si lo que cambió pertenece a la parte nativa.

En el **flujo CNG mostrado**, el equipo conserva la configuración y regenera `android/` e `ios/`. **Una regeneración limpia puede descartar ediciones manuales** de esos proyectos. Esto no significa que toda ejecución de `prebuild` borre siempre las carpetas ni que nunca corresponda versionarlas: importa cuál es la fuente de verdad y cómo administra el proyecto sus cambios nativos. **Fuentes: U04 - T01.2, 09:12–11:28; contraste: Permisos, pp. 11–16.** El comando sin `--clean` de la demostración y el ejemplo con `--clean` del PDF mantienen su atribución separada.

El repaso del 08/10 concreta ese riesgo: **una configuración editada solo en un archivo nativo generado puede perderse al regenerarlo**. Se relaciona con la elección de la fuente de verdad descrita aquí, sin interpretar que cualquier recarga o cualquier `prebuild` borre siempre toda modificación. **Fuente: Clase 08/10/2026, aproximadamente 02:03–27:30.**

## 3. Permisos: declarar, solicitar y manejar el rechazo

T01.2 alcanza a enunciar la secuencia **declarar el permiso → solicitarlo → mantener la app utilizable si el usuario lo deniega**. El texto se corta en medio de una frase a **11:43**; no se da por desarrollado todo el tema en ese fragmento. La explicación detallada y los ejemplos siguientes conservan sus referencias al PDF. **Fuente del inicio audiovisual: U04 - T01.2, 11:34–11:43.**

Son dos momentos diferentes:

1. **Declaración de compilación:** el binario declara qué capacidades podrá solicitar mediante manifiestos y configuración.
2. **Solicitud de ejecución:** el código consulta o pide permiso y el usuario decide mediante un diálogo del sistema.

Para las capacidades que requieren ambos pasos, declarar no equivale a obtener autorización. **Fuente: Permisos, p. 18.**

T01.3 lo relaciona con una acción concreta: **el usuario inicia el escaneo de un QR** y entonces la app solicita acceso a la cámara. La configuración nativa declara qué acceso puede pedir, pero **no concede ese permiso**. La solicitud durante la ejecución permite que el usuario decida en el momento en que entiende para qué se necesita. **Fuente: U04 - T01.3, 00:27–02:17.**

**Precisión editorial:** los fallos mencionados en la explicación de clase no se convierten en un comportamiento idéntico de todas las APIs de iOS y Android. El contraste que se conserva es declaración frente a autorización efectiva; los detalles de cada capacidad dependen de su módulo y plataforma.

Los estados presentados son `undetermined`, `granted` y `denied`. `canAskAgain: false` indica que no se puede resolver repitiendo el diálogo y debe orientarse al usuario hacia Ajustes. **Fuente: Permisos, p. 19.**

```tsx
const [permiso, pedirPermiso] = useCameraPermissions();

if (!permiso) return <View />;
if (!permiso.granted) {
  return (
    <View>
      <Text>Necesitamos la cámara para la foto del producto.</Text>
      <Button title="Dar acceso" onPress={pedirPermiso} />
    </View>
  );
}
return <CameraView style={{ flex: 1 }} facing="back" />;
```

**Fuente: Permisos, p. 20.** Las tres ramas distinguen resolución inicial, falta de autorización y acceso concedido. El ejemplo básico debe combinarse con el tratamiento de `canAskAgain` descrito en la p. 19.

### Pantalla de cámara: carga, decisión y rechazo

El ejemplo de **`useCameraPermissions` de `expo-camera`** permite separar dos situaciones que no deben confundirse: **el hook todavía está resolviendo** y aún no tiene respuesta, o **ya devolvió `undetermined`**, que informa que el usuario todavía no decidió. La primera es carga; la segunda ya permite explicar el propósito y ofrecer la solicitud. **Fuente: U04 - T01.3, 02:27–05:04.**

| Situación | Qué debe ofrecer la pantalla |
| --- | --- |
| Cargando: todavía no hay respuesta del hook | Una indicación de espera, sin presentar prematuramente un rechazo. |
| Sin decisión previa: `undetermined` | Explicar por qué se necesita la cámara y ofrecer un botón que active la solicitud del sistema. |
| Concedido: `granted` | Habilitar la cámara. |
| Denegado y `canAskAgain: true` | Ofrecer un reintento voluntario y mantener una alternativa útil; no solicitar repetidamente sin intervención del usuario. |
| Denegado y `canAskAgain: false` | Evitar repetir una solicitud que ya no mostrará el diálogo y conservar una alternativa para continuar. |

**Fuente: U04 - T01.3, 02:27–05:04; contraste con Permisos, pp. 19–20.** El cuadro amplía el fragmento básico del PDF que se conserva arriba: allí `!permiso` devuelve una `View` vacía y todos los casos no concedidos se agrupan. Ese fragmento ilustra el mecanismo, pero **no representa por sí solo toda la experiencia de espera y rechazo** descrita aquí.

Las funciones `get...PermissionsAsync()` consultan; `request...PermissionsAsync()` solicitan. En iOS se explican textos de propósito como `NSCameraUsageDescription` y `NSLocationWhenInUseUsageDescription`. En Android, `permissions` agrega y `blockedPermissions` excluye permisos incorporados por librerías que no se utilizan. **Fuente: Permisos, pp. 21–23.**

### Ubicación sin hook

T01.3 explica la alternativa con funciones: solicitar ubicación en primer plano mediante **`requestForegroundPermissionsAsync`** y llamar a **`getCurrentPositionAsync` solo si se concedió**. Se registra como ejemplo explicado en clase, **sin atribuir una prueba real de GPS**. La sección 5 desarrolla el recorrido de ubicación y sus ejemplos del PDF, por lo que no se repiten aquí. **Fuente: U04 - T01.3, 05:07–05:43.**

### Configuración por plataforma: propósito y permisos innecesarios

Para iOS, el texto de propósito debe expresar una acción comprensible: **«Usamos la cámara para escanear el código QR»**. Se relaciona con **`NSCameraUsageDescription`** y con la opción **`cameraPermission`** del plugin, manteniendo la grafía de las fuentes locales. El texto explica al usuario el motivo; no reemplaza su decisión. **Fuentes: U04 - T01.3, 05:53–08:10; Permisos, pp. 14 y 22.**

En Android se retoma una app que **solo toma fotos**. Si una librería incorpora grabación de audio que ese caso no utiliza, **`android.blockedPermissions`** permite excluir **`android.permission.RECORD_AUDIO`**. No es una indicación de quitarlo si el proyecto sí necesita grabar: el criterio es ajustar permisos a las funciones reales. **Fuentes: U04 - T01.3, 05:53–08:10; Permisos, p. 23.**

El manifiesto `PrivacyInfo.xcprivacy`, generado desde `ios.privacyManifests`, describe usos de APIs para Apple; no es el texto del diálogo al usuario. La fuente remite su revisión de entrega a la Unidad 7. **Fuente: Permisos, p. 24.**

El video trata este manifiesto **por separado de los permisos solicitados al usuario**: documenta motivos de uso de determinadas APIs y **no concede acceso ni sustituye el diálogo de autorización**. No deben confundirse `ios.privacyManifests`, las descripciones de uso y el estado que devuelve la solicitud en ejecución. **Fuente: U04 - T01.3, 05:53–08:10; nombres contrastados con Permisos, pp. 22–24.**

La regla práctica de la cátedra es pedir permiso al realizar una acción concreta, explicar el motivo y conservar una alternativa: elegir una foto, escribir una dirección o continuar sin la capacidad. Se evalúa que la app siga siendo utilizable ante el rechazo. **Fuente: Permisos, p. 25.**

T01.3 cierra con **tocar «Sacar foto» → explicar el motivo → solicitar acceso**. Si el usuario lo rechaza, se puede ofrecer **elegir una imagen de la galería cuando esa opción esté disponible**. La alternativa no se presupone autorizada ni viable en cualquier contexto: debe permitir continuar de forma útil en el caso concreto, sin dejar una pantalla en blanco. **Fuente: U04 - T01.3, 08:16–09:02.**

El repaso del 08/10 aporta otra alternativa de diseño: **un mapa centrado en coordenadas conocidas puede mostrarse aunque el usuario deniegue acceso a su ubicación**. Mostrar ese lugar no equivale a leer la posición actual de la persona. Se vincula con la sección 5, sin convertir el permiso de ubicación en requisito de toda visualización de un mapa. **Fuente: Clase 08/10/2026, aproximadamente 02:03–27:30.**

## 4. Cámara, galería y códigos

| Necesidad | Solución de la clase |
| --- | --- |
| Vista previa dentro de la pantalla, control de cámara o lectura de códigos | `expo-camera` y `CameraView`. |
| Selección con interfaz del sistema y posible recorte | `expo-image-picker`. |

El picker también puede abrir la cámara del sistema. El material recomienda comenzar por él si no se necesita una vista propia. **Fuente: APIs, p. 4.**

### Elegir la herramienta según el PRD

La clase del 08/10 compara dos maneras de resolver la captura: **`expo-image-picker`** permite elegir una imagen de la galería o abrir **la cámara del sistema**; **`expo-camera`** permite integrar **`CameraView` en una pantalla propia**, controlar la captura mediante una referencia y leer QR. La decisión depende de si el PRD necesita una selección/captura con interfaz del sistema o una experiencia de cámara integrada y personalizada. **Fuente: Clase 08/10/2026, 28:21–35:40.**

En esta clase **se demuestra ImagePicker**. `CameraView`, la captura por referencia y el escaneo se explican como alternativas: los ejemplos de estas últimas capacidades que se conservan a continuación siguen atribuidos al PDF, no se dan por ejecutados en el video. **Fuentes: Clase 08/10/2026, 28:21–35:40; APIs, pp. 5–7.**

Con `CameraView`, `facing` elige frontal o trasera y los hijos permiten superponer botones. Para tomar una foto se conserva una referencia y se llama:

```tsx
const resultado = await camara.current?.takePictureAsync({ quality: 0.7 });
setFoto(resultado?.uri ?? null);
```

El resultado incluye URI y dimensiones; opcionalmente base64, que aumenta el tamaño. La foto está en caché, por lo que debe copiarse si se necesita conservarla. **Fuente: APIs, pp. 5–6.**

Para QR y barras se configura `barcodeScannerSettings` y `onBarcodeScanned`. La lectura puede repetirse mientras el código esté visible: el ejemplo usa una bandera `escaneado` para no navegar repetidamente. Propone inventario, entradas, menús y asistencia como usos. **Fuente: APIs, p. 7.**

### Escáner QR del medidor dentro de la app

T01.4 retoma el caso de medidores desde otra necesidad: el 08/10 se abría **la cámara del sistema para tomar una foto**, mientras que ahora se prepara un escáner con **`CameraView` de `expo-camera` dentro de la aplicación**. La finalidad es **validar el medidor** a partir del código leído, no solamente obtener una imagen. **Fuente: U04 - T01.4, inicio–aproximadamente 35:30; relación con Clase 08/10/2026, 28:21–35:40.**

El componente de escaneo se muestra en un **modal**, solicita el permiso de cámara y limita la lectura al **tipo QR**. La pantalla que abre el escáner le pasa un **callback**, al que se entrega el dato leído. Así se separa reconocer un código de decidir qué hacer con ese dato en la pantalla del suministro. **Fuente: U04 - T01.4, inicio–aproximadamente 35:30.**

Se conserva un estado de **«escaneado»** porque el evento puede repetirse mientras el QR siga delante de la cámara. Ese estado evita procesar varias veces una misma lectura; para otra lectura hay que **volver a habilitar el escaneo**. No se inventa un formato de QR ni un contrato de validación no recibido. **La lectura física no quedó comprobada en esta clase**: el armado del componente y su flujo no demuestran por sí solos reconocimiento real ni validación exitosa de un medidor. **Fuente: U04 - T01.4, inicio–aproximadamente 35:30; contraste: APIs, p. 7.**

```tsx
const resultado = await ImagePicker.launchImageLibraryAsync({
  mediaTypes: ['images'],
  allowsEditing: true,
  aspect: [4, 3],
  quality: 0.8,
});
if (resultado.canceled) return;
const imagen = resultado.assets[0];
setUri(imagen.uri);
```

**Fuente: APIs, p. 8.** El material utiliza arrays de tipos de medios y `canceled` con una sola `l`. El asset puede incluir tamaño, MIME, nombre y EXIF. Para mostrarlo utiliza `expo-image`; para imágenes grandes antes de subirlas menciona `expo-image-manipulator`. **Fuente: APIs, p. 9.**

### Contexto de captura: rutas de lectura y suministro

La práctica retoma la **app de medidores** presentada en Unidad 3. Se cargan rutas de lectura con **datos simulados**, se muestran en `FlatList` y se navega por identificador hasta el suministro donde se adjunta la foto. Este recorrido explica desde qué tarea llega el usuario a la captura, sin volver a desarrollar listas y navegación. **Fuente: Clase 08/10/2026, 45:37–1:03:35.**

El ejemplo funciona con **datos locales**: recorrer las pantallas no demuestra consumo de una API ni sincronización de registros de medidores. Se conserva esa diferencia entre contexto del caso, demostración y funcionalidades futuras.

### Preparación del módulo y selección desde galería

Se observa un error al **agregar el plugin en `app.json` antes de instalar el paquete**: el proyecto no puede cargar el módulo. El caso relaciona dependencia instalada y configuración, sin transformar el texto de un error particular en una regla universal de todas las herramientas. **Fuente: Clase 08/10/2026, 1:03:35–1:34:29; relación con la sección 2.**

En el flujo de galería de la demostración se **comprueba el permiso**, se abre el selector y se revisa si el usuario **canceló antes de leer `assets[0]`**. **Cancelar una selección no es denegar un permiso**: el usuario puede abandonar el selector sin elegir una imagen aun teniendo acceso autorizado. El fragmento del PDF anterior conserva ese orden al comprobar `resultado.canceled`. La consulta de permiso de la demo no se generaliza aquí a cualquier versión o selector del sistema. **Fuente: Clase 08/10/2026, 1:03:35–1:34:29.**

### Cámara del sistema, rechazo y Ajustes

Para la cámara, la solicitud se realiza **al tocar el botón**. Ante una denegación se presenta una explicación. Cuando el sistema deja de mostrar el diálogo, el docente habilita el acceso desde **Ajustes**. Esto se vincula con **`canAskAgain`** y las ramas de la sección 3: repetir la petición cuando ya no puede mostrarse no resuelve el estado. **Fuente: Clase 08/10/2026, 1:03:35–1:34:29.**

**Precisión editorial:** no se adopta un reintento recursivo como solución. Debe respetarse la decisión del usuario y conservar una explicación y un camino útil; la habilitación manual observada en Ajustes no significa que la aplicación pueda concederse el permiso por sí misma.

### Resultado visible y límites de la demostración

El resultado se guarda como **asset en el estado** y se utiliza **su URI para mostrar la foto con dimensiones definidas**. La demostración llega hasta la **vista previa local**, no hasta un envío o almacenamiento remoto confirmado. **Fuente: Clase 08/10/2026, 1:03:35–1:34:29.**

El envío a una API, Base64, el redimensionamiento y el almacenamiento remoto se discuten como **opciones**. No se les atribuye código ejecutado ni un backend implementado. Tampoco guardar el asset en estado garantiza conservar su archivo entre aperturas: la distinción de archivos temporales y permanentes se mantiene en la sección 7. **Fuentes: Clase 08/10/2026, 1:03:35–1:34:29; contraste: APIs, pp. 6 y 29.**

### Cierre de clase y alcance de entrega

En el cierre se presenta el **APK de producción como un extra**. Esa mención se conserva por separado de la indicación previa del **build de preview**, documentada en las orientaciones del integrador y en Unidad 7; no se interpreta como sustitución de esa entrega ni se fijan fechas a partir de estimaciones orales. Las **notificaciones push se anuncian para otra clase**, no se implementan en este video. **Fuente: Clase 08/10/2026, 1:35:00–1:43:00.**

## 5. Ubicación y mapas

La clase diferencia permiso de ubicación en primer plano y en segundo plano; utiliza el primero para las prácticas y desaconseja pedir el segundo sin una necesidad concreta. **Fuente: APIs, p. 11.**

La lectura combina una ubicación previa, rápida pero posiblemente vieja, con una actual:

```ts
const { status } = await Location.requestForegroundPermissionsAsync();
if (status !== 'granted') return null;
const ultima = await Location.getLastKnownPositionAsync();
if (ultima) mostrar(ultima);
const actual = await Location.getCurrentPositionAsync({
  accuracy: Location.Accuracy.Balanced,
});
mostrar(actual);
```

**Fuente: APIs, p. 12.** La precisión y la espera son parte de la experiencia, no solo del acceso al GPS.

### Posición del lector al registrar una lectura

El caso de T01.4 plantea conocer **dónde estaba el lector cuando registró la lectura**. Con `expo-location` se solicita permiso **en primer plano**, se obtiene una **posición puntual** y se consultan **latitud y longitud**. Se registra una **prueba con ubicación simulada**, no una medición real de la posición de un lector junto al medidor. **Fuente: U04 - T01.4, aproximadamente 36:30–53:30.**

Esta consulta puntual se distingue del **seguimiento por cambios de posición** y del **acceso en segundo plano**, explicados como opciones para otros requisitos. La práctica tampoco demuestra una **validación de proximidad contra el medidor**: obtener coordenadas no equivale a compararlas con la ubicación del suministro y aceptar o rechazar la lectura por distancia. El seguimiento descrito a continuación conserva su fuente de PDF. **Fuente: U04 - T01.4, aproximadamente 36:30–53:30.**

`watchPositionAsync` permite seguir cambios con precisión e intervalo de distancia. Hay que conservar la suscripción y llamar a `remove()` para dejar de escuchar. El momento de limpieza debe corresponder al ciclo de vida necesario: montaje, foco o estado de la app. **Fuentes: APIs, p. 13; Unidad 2, sección de ciclos de vida.**

**Aclaración editorial:** el ejemplo de la p. 13 instala la suscripción de forma asíncrona. Su limpieza abreviada no desarrolla qué sucede si la pantalla se desmonta antes de que se resuelva la solicitud. No se presenta como un manejo completo de todas las carreras de ejecución.

`geocodeAsync` convierte dirección en coordenadas y `reverseGeocodeAsync` hace lo inverso. Los ejemplos utilizan Paraná, Entre Ríos; ambos métodos devuelven arreglos que pueden estar vacíos. **Fuente: APIs, p. 14.**

La herramienta elegida es `react-native-maps`, con `MapView`, `Marker`, `Polyline`, `Polygon` y `Circle`. La región inicial utiliza latitud, longitud y deltas; el círculo expresa su radio en metros. Se diferencia probar con Expo Go de preparar credenciales propias para una build de producción. `expo-maps` se menciona como alternativa que la fuente considera alpha y no adopta como base. **Fuente: APIs, pp. 15–17.**

Ante la consulta sobre **un mapa que no se veía**, el docente sugiere revisar **las dimensiones del contenedor y del propio mapa**. Las claves de Google y el despliegue se comentan **sin una prueba concluyente**, por lo que no se registra una configuración resuelta ni se atribuye una causa definitiva al problema. **Fuente: Clase 08/10/2026, 1:35:00–1:43:00.**

### Mapa de suministros: toques, marcadores y figuras

T01.4 utiliza **`react-native-maps`** dando a **`MapView` dimensiones visibles** y definiendo una **región inicial**. La práctica obtiene las coordenadas de un toque sobre el mapa y las utiliza para **agregar marcadores**. Esas coordenadas elegidas en el mapa no deben confundirse con la posición del dispositivo consultada antes. **Fuente: U04 - T01.4, aproximadamente 53:30–1:24:30.**

| Figura | Qué representa en el ejemplo |
| --- | --- |
| `Marker` | Un punto geográfico. |
| `Polyline` | Una línea que une los puntos proporcionados en orden. |
| `Polygon` | Un área cerrada a partir de los puntos. |

**Fuente: U04 - T01.4, aproximadamente 53:30–1:24:30; contraste: APIs, p. 15.** La línea dibujada **une las coordenadas dadas; no calcula un recorrido por calles**. No se deduce un servicio de rutas ni una optimización del itinerario de lectura.

Se consulta cómo evitar **marcadores duplicados**. Se conserva esa cuestión de control de los puntos agregados, sin afirmar que la demostración haya resuelto todos los casos posibles de duplicación. No se reconstruye un algoritmo de comparación o tolerancia espacial ausente de los aportes recibidos. **Fuente: U04 - T01.4, aproximadamente 53:30–1:24:30.**

**Aclaración editorial:** APIs, p. 16, escribe `"process.env.GOOGLE_MAPS_KEY"` dentro de un JSON. Eso es texto literal, no una lectura automática de la variable. La intención de utilizar configuración por entorno se conserva, pero ese bloque no es una implementación completa de sustitución de variables.

## 6. Sensores y hápticos

`expo-sensors` agrupa capacidades diferentes:

| Sensor | Dato que describe la presentación |
| --- | --- |
| Acelerómetro | Aceleración en ejes x, y, z, expresada en g. |
| Giroscopio | Velocidad de rotación en rad/s. |
| Magnetómetro | Campo magnético en μT. |
| Barómetro | Presión en hPa. |
| Sensor de luz | Iluminación en lux; la fuente lo ubica en Android. |
| Podómetro | Pasos. |
| DeviceMotion | Datos de movimiento combinados y procesados. |

**Fuente: APIs, p. 19.** La disponibilidad varía y debe comprobarse en hardware real.

El patrón es **consultar disponibilidad → fijar frecuencia → suscribirse → retirar la suscripción**. El acelerómetro del ejemplo usa `isAvailableAsync()`, `setUpdateInterval(100)` y `addListener`, conservando el objeto para `remove()`. **Fuente: APIs, p. 20.**

Para detectar una sacudida se calcula `Math.sqrt(x*x + y*y + z*z)` y se compara con `1.8`. El ejemplo responde con feedback de éxito y sortea una pregunta. Es una demostración: no incluye una ventana de bloqueo para impedir varios disparos de la misma sacudida. **Fuente: APIs, p. 21.**

Los hápticos distinguen selección (`selectionAsync`), resultado de una acción (`notificationAsync`) e impacto (`impactAsync`). La presentación menciona una API específica para Android y condiciones que pueden impedir la vibración en iOS. La señal táctil no debe ser la única forma de informar el resultado. **Fuente: APIs, p. 22.**

## 7. Archivos: objetos, ubicación y permanencia

La API utilizada en el material se basa en `File`, `Directory` y `Paths`, en lugar de funciones sueltas sobre URI. Se menciona el import `/legacy` como transición para código anterior. **Fuente: APIs, pp. 24–25.**

| Ubicación | Uso |
| --- | --- |
| `Paths.document` | Datos que la app debe conservar, como notas o fotos propias. |
| `Paths.cache` | Recursos temporales o recuperables; el sistema puede borrarlos. |

**Fuente: APIs, p. 26.**

```ts
import { File, Directory, Paths } from 'expo-file-system';

const carpeta = new Directory(Paths.document, 'notas');
if (!carpeta.exists) carpeta.create();
const archivo = new File(carpeta, 'clase-09.md');
archivo.create({ overwrite: true });
archivo.write('# Unidad 4');
console.log(await archivo.text());

for (const item of carpeta.list()) {
  if (item instanceof File) console.log(item.name, item.size);
}
```

**Fuente: APIs, p. 27, con la lectura asíncrona que también incluye la diapositiva.** Para operaciones pequeñas se muestran variantes síncronas; con archivos grandes pueden bloquear la interfaz.

La p. 28 presenta `File.downloadFileAsync` para descarga completa y `File.createDownloadTask` con `onProgress` para informar avance; también menciona `watch`. Se registran como APIs del PDF, sin prueba de compatibilidad con una instalación concreta.

El ejemplo que cierra el tema copia una foto temporal a documentos y devuelve la nueva URI:

```ts
async function guardarFoto(uriDeLaCamara: string) {
  const galeria = new Directory(Paths.document, 'fotos');
  if (!galeria.exists) galeria.create();
  const temporal = new File(uriDeLaCamara);
  const definitiva = new File(galeria, `${Date.now()}.jpg`);
  temporal.copy(definitiva);
  return definitiva.uri;
}
```

Guardar solamente una URI temporal en la base de datos no conserva el archivo. **Fuente: APIs, p. 29.**

## 8. Multimedia

La presentación separa **reproductor**, objeto con estado propio, de **vista**, componente que lo muestra. Utiliza `expo-video` y `expo-audio` y advierte sobre ejemplos antiguos con `expo-av`. Cambiar una propiedad del reproductor no equivale a cambiar estado React: para reflejar la reproducción en la pantalla se escuchan eventos. **Fuente: APIs, pp. 31–32.**

Para video muestra `useVideoPlayer`, `VideoView` y `useEvent(player, 'playingChange', ...)`, con acciones `play()` y `pause()`. Segundo plano y picture-in-picture requieren configuración nativa según la fuente. **Fuente: APIs, p. 32.**

Para audio, `useAudioPlayer` reproduce un recurso; `useAudioRecorder` y `useAudioRecorderState` coordinan la grabación. Se pide permiso de micrófono, se prepara, se inicia con `record()` y se termina con `stop()`. El resultado está en una URI que debe conservarse si se quiere superar la vida de la caché. **Fuente: APIs, p. 33.**

## 9. Notificaciones locales y push

En el cierre de **T01.4** se presenta la **API de ejemplo de la cátedra**, las opciones de ejecución local con **Docker Compose** y la documentación **Swagger/OpenAPI**. La **conexión de la app y las notificaciones se anuncian para una clase posterior**; no se registran como integración efectuada en esta práctica. No se inventan comandos, endpoints ni un resultado de despliegue. **Fuente: U04 - T01.4, aproximadamente 1:24:30–1:31:08, cierre textual recibido.**

La teoría y los ejemplos de notificaciones que siguen **conservan la atribución al PDF Notificaciones**. El anuncio de otra clase no abre una búsqueda de un sexto video ni impide cerrar los cinco materiales audiovisuales confirmados.

Una notificación es una presentación del sistema: la app aporta contenido y datos, pero el sistema controla su representación. La clase insiste en el costo de perder el permiso por abuso. **Fuente: Notificaciones, p. 4.**

| Local | Push |
| --- | --- |
| La programa la app en el dispositivo. | La envía un servidor. |
| No necesita servidor ni internet para dispararse. | Necesita conexión, token y credenciales. |
| Recordatorios, temporizadores, vencimientos. | Mensajes y cambios externos de estado. |
| Se utiliza para comenzar en Expo Go. | El flujo de la clase utiliza development build. |

**Fuente: Notificaciones, pp. 5–6.** La push silenciosa se menciona como fuera del alcance de la materia.

### Handler, permisos y canales

Con la app abierta se define cómo presentar mediante un handler, declarado una vez fuera del componente:

```ts
Notifications.setNotificationHandler({
  handleNotification: async () => ({
    shouldShowBanner: true,
    shouldShowList: true,
    shouldPlaySound: true,
    shouldSetBadge: false,
  }),
});
```

**Fuente: Notificaciones, pp. 7 y 10.** Con la app minimizada o cerrada interviene la presentación del sistema.

En Android se crea un canal antes de solicitar el permiso, utilizando `setNotificationChannelAsync`. Los canales son categorías que el usuario puede silenciar independientemente. Después se consulta con `getPermissionsAsync` y, si corresponde, se solicita con `requestPermissionsAsync`. Ícono, color y sonidos del plugin pertenecen al binario y requieren recompilación al cambiarlos. **Fuente: Notificaciones, pp. 9 y 11.**

### Programar y administrar

```ts
const id = await Notifications.scheduleNotificationAsync({
  content: {
    title: 'Listo',
    body: 'Se guardó tu entrega.',
    data: { ruta: '/entregas/42' },
  },
  trigger: null,
});
```

La fuente utiliza `null` para inmediata y objetos con `type` para intervalos y fechas: `TIME_INTERVAL` o `DATE`. El ejemplo periódico es cada `60 * 20` segundos. **Fuente: Notificaciones, pp. 12–13.**

Guardar `id` permite cancelar una notificación concreta. `cancelScheduledNotificationAsync` y `cancelAllScheduledNotificationsAsync` eliminan programaciones; `dismissAllNotificationsAsync` retira avisos ya mostrados. Editar un recordatorio sin cancelar el anterior puede duplicarlo. **Fuente: Notificaciones, p. 14.**

Se distinguen el listener de llegada y el de respuesta del usuario. El ejemplo guarda una ruta en `data` y navega al tocar el aviso; ambos listeners se eliminan en la limpieza. **Fuente: Notificaciones, p. 15.** **Aclaración editorial:** la diapositiva no desarrolla por separado la recuperación de la respuesta inicial al arrancar desde un proceso cerrado; el fragmento no agota todos los casos de inicio de la aplicación.

### Recorrido de una push

La cadena es **app → servidor propio → Expo Push Service → FCM/APNs → dispositivo**. La app obtiene permiso y token; el servidor asocia tokens a usuarios y decide destinatarios y momento del aviso. **Fuente: Notificaciones, p. 17.**

El registro del ejemplo verifica dispositivo y permiso, obtiene `projectId`, llama a `getExpoPushTokenAsync({ projectId })` y envía el token al backend. Requiere configuración de proyecto, development build y credenciales; no alcanza con copiar el token a un componente. **Fuente: Notificaciones, pp. 18–20.**

El servidor puede utilizar `expo-server-sdk`, validar tokens, dividir mensajes en lotes y enviar. La presentación muestra también una petición de prueba a `https://exp.host/--/api/v2/push/send`. Es un ejemplo documental: no se enviaron notificaciones. **Fuente: Notificaciones, pp. 21–22.**

### Tickets, recibos y diagnóstico

| Resultado | Qué significa según el material |
| --- | --- |
| Ticket inmediato con `ok` | Expo aceptó el mensaje; no demuestra que el usuario lo recibió. |
| Recibo posterior | Informa el resultado del servicio de entrega. |
| `DeviceNotRegistered` | Retirar el token inválido del servidor. |
| `MessageTooBig` | Reducir el payload; enviar identificadores. |
| `MessageRateExceeded` | Reintentar con espera creciente. |
| `MismatchSenderId` | Revisar correspondencia de credenciales FCM y proyecto. |

**Fuente: Notificaciones, pp. 23–24.** Los tokens asociados a usuarios, la decisión de envío y las credenciales pertenecen al servidor; la lista completa no se expone públicamente. **Fuente: Notificaciones, p. 25.**

**Diferencia interna de la fuente:** el ejemplo de registro rechaza lo que no sea dispositivo físico (p. 18), mientras la p. 20 enumera opciones de emulación/simulación. Se conserva el ejemplo con su restricción, sin atribuirle cobertura de todos esos entornos.

Al diagnosticar, primero revisar app en primer plano sin handler, permiso, Expo Go frente a push y modo no molestar; después token, prueba aislada, recibos y credenciales. Las buenas prácticas son avisos pedidos o relevantes, agrupación, respeto de horario y preferencias, y permiso solicitado en contexto. **Fuente: Notificaciones, pp. 27–28.**

## Cierre y limitaciones de las fuentes

- Los tres PDF quedaron integrados con referencias y ejemplos de sus distintos temas.
- Los requisitos de tiendas y compatibilidades se registran como contenido de las fuentes, sin revisión normativa o técnica externa.
- Se conserva el enlace identificado para esta unidad: <https://drive.google.com/file/d/1pPvScJIo_8Y_pks_GwhJFawkQLyAog9w/view>. Su contenido no se consultó ni se dedujo.
- **Estado audiovisual: 5 de 5 videos incorporados.** Se verificaron **U04 - T01.1, T01.2, T01.3, la clase del 08/10/2026 y T01.4**, cada uno con su enlace del campus y sus tiempos. No quedan videos por incorporar del listado confirmado.
- La transcripción de U04 - T01.1 se corta a **12:22, a mitad de una explicación** sobre la comparación con tareas nativas manuales. No se registra ese punto como final de la grabación ni se da por desarrollado todo el flujo de plugins y permisos en el video.
- T01.2 confirma la interrupción de la grabación anterior y reinicia el contador. Su texto termina en **11:43, en medio de una frase**. Amplía prebuild, archivos nativos, plugin de cámara y necesidad de recompilar; el flujo de permisos solo se inicia y su desarrollo escrito sigue atribuido al PDF.
- T01.3 amplía la sección de permisos: carga inicial frente a `undetermined`, concesión y rechazo con `canAskAgain`, ubicación sin hook y diferencias de configuración por plataforma. Se registra **9:23 de duración del reproductor**, **9:16 como última marca de transcripción** y despedida, según lo informado. No se atribuye una prueba real de GPS.
- La clase del **08/10/2026** llega a **1:43:00 e incluye la despedida**, según la transcripción identificada por el usuario. Demuestra ImagePicker y vista previa local en el caso de medidores; CameraView y QR son alternativas explicadas. API, Base64, redimensionamiento y almacenamiento remoto se discuten sin darse por implementados; push se anuncia para otra clase.
- **T01.4** amplía el escáner QR en modal, la ubicación puntual del lector con posición simulada y el mapa con marcadores, líneas y polígonos. La lectura física del QR, la validación de proximidad y un recorrido por calles no quedan demostrados. La API de ejemplo se presenta; la conexión de la app y notificaciones se anuncian para después.
- Para T01.4 se registra **1:31:15 de duración indicada** y **1:31:08 como última marca de transcripción, con cierre**. Los cortes de T01.1 y T01.2 se conservan y no se completa el texto ausente.
- El enlace de Drive permanece **sin identificar y separado**, como limitación de las fuentes: no se asocia a T01.4 ni se cuenta como un sexto video. No bloquea el cierre.

La Unidad 4 queda como **Documentación completa respecto del material disponible**, con **5 de 5 videos incorporados**, los tres PDF conservados y sus límites de cobertura explícitos.
