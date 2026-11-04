# Unidad 7 — Construcción, publicación y actualización

[Volver al índice](00_INDICE.md)

**Estado: Documentación completa respecto del material disponible. Audiovisuales: 2 de 2 videos incorporados.** Se conservan los dos PDF y los aportes de **U07.T01 – Construir la Aplicación**, y se integra **U07.T02 – Publicar la Aplicación**. Se verificaron ambas fuentes en este documento; no quedan videos pendientes para la Unidad 7. Los límites de las demostraciones y la atribución de condiciones comerciales se conservan.

## Fuentes y alcance

| Referencia | Fuente original | Páginas |
| --- | --- | --- |
| **Construcción** | [Unidad 7 — Construir la aplicación · Desarrollo para Móviles.pdf](../fuentes/pdf/Unidad%207%20%E2%80%94%20Construir%20la%20aplicaci%C3%B3n%20%C2%B7%20Desarrollo%20para%20M%C3%B3viles.pdf) | 27 |
| **Publicación** | [Unidad 7 — Publicar y actualizar.pdf](../fuentes/pdf/Unidad%207%20%E2%80%94%20Publicar%20y%20actualizar.pdf) | 28 |

El programa, p. 3, incluye preparación de activos y construcción de aplicaciones para producción dentro de publicación en tiendas. Los PDF amplían envío, actualización, monitoreo y entrega del integrador. Se cita la página del visor, incluida la portada. Los comandos son documentación: no se compilaron, firmaron, subieron ni publicaron aplicaciones.

**Primera fuente audiovisual:** [U07.T01 – Construir la Aplicación](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=56574), cuyo archivo se identifica como **«U07.T01 - Publicación de la Aplicación en la Tienda.mp4»**. Se registran ambos títulos como **una sola fuente**, no como dos grabaciones. Fecha no informada; duración indicada del reproductor **47:43** y última marca de transcripción **47:40**.

**Segunda fuente audiovisual:** [U07.T02 – Publicar la Aplicación](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=56597), archivo **«U07.T02 - Publicación de la Aplicación en la Tienda.mp4»**. Fecha no informada; duración indicada del reproductor **32:09** y última marca de transcripción **32:08**. Los tiempos son propios de T02. El enlace no pudo consultarse desde la herramienta disponible: se integran los aportes recibidos, sin afirmar una revisión directa del video ni reconstruir texto ausente.

**Alcance de integración:** se utilizan los aportes y marcas recibidos, no una revisión directa del video ni su código literal completo. El enlace no pudo consultarse desde la herramienta disponible. La demostración del docente se distingue de la elaboración de estos apuntes: aquí no se ejecutaron compilaciones ni se utilizaron cuentas. Las condiciones comerciales mencionadas se atribuyen al contexto de clase, sin validación actual.

**Criterio de lectura:** las tarifas, cupos, fechas y políticas se conservan como información de las presentaciones de la cátedra. No se verificaron contra servicios o tiendas actuales y no deben confundirse con condiciones comprobadas para una publicación real.

## 1. Del proyecto al binario

En debug se utiliza Metro y hay herramientas de desarrollo. En release, el JavaScript del proyecto queda empaquetado, optimizado y, en el entorno de la clase, convertido a bytecode de Hermes. La aplicación instalada puede funcionar sin la computadora del desarrollador. **Fuente: Construcción, p. 4.**

### Formatos

| Formato | Uso explicado por la fuente |
| --- | --- |
| `.aab` | Android App Bundle enviado a Play; la tienda genera APK adecuados a los dispositivos. No se instala directamente como un APK. |
| `.apk` | Instalable Android para pruebas y distribución directa. |
| `.ipa` | Paquete de iOS para sus mecanismos de distribución. |

**Fuente: Construcción, p. 5.**

**Aclaración editorial:** esa página presenta App Store/TestFlight como vías de iOS y dice que no se copia el archivo para instalarlo. La misma fuente desarrolla después distribución ad hoc (pp. 16 y 22). Los apuntes conservan también ese caso, sin interpretar la primera enumeración como la única modalidad posible.

La clase relaciona el artefacto con su destinatario: **APK para instalar directamente en Android**, **AAB para el circuito de Google Play** e **IPA para la distribución iOS bajo sus condiciones**. La extensión no basta para saber si la app necesita Metro: también importa cómo se construyó. El APK de esta demostración es de **development**, no una prueba autónoma de preview. **Fuente: U07.T01, aproximadamente 00:00–12:20; relación con la elección de perfiles de 12:20–19:55.**

### Para qué se firma

La firma se relaciona con identidad, integridad y continuidad de actualizaciones. La aplicación que recibe el usuario debe poder reconocerse como una actualización autorizada de la instalada. Por eso las credenciales de firma no son archivos accesorios. **Fuente: Construcción, p. 6.**

En Android se distinguen:

- **Clave de carga:** identifica el envío del desarrollador a Google Play; la fuente señala la posibilidad de restablecimiento.
- **Clave de firma de la app:** corresponde a los APK distribuidos por Play dentro del mecanismo que administra Google.

El **keystore** es el archivo que contiene material de claves y certificados, protegido por contraseña. **Fuente: Construcción, p. 7.**

En iOS se explican el **certificado de distribución**, que identifica al firmante, y el **perfil de aprovisionamiento**, que relaciona aplicación, firma y destinos de ejecución, incluidos dispositivos autorizados para ciertas pruebas. **Fuente: Construcción, p. 8.**

El repaso audiovisual vincula la **firma con la continuidad de las actualizaciones**. En Google Play distingue la **clave de subida** —la clave de carga del cuadro conceptual anterior— de la **clave de firma de la app** distribuida; en iOS mantiene separadas la función del certificado y la del perfil de provisión o aprovisionamiento. Conocer qué pieza identifica cada etapa evita tratar todas las credenciales como si fueran intercambiables. **Fuente: U07.T01, aproximadamente 00:00–12:20.**

## 2. EAS Build, perfiles y credenciales

La presentación separa tres servicios de Expo Application Services: **Build** compila y firma, **Submit** envía binarios y **Update** distribuye cambios compatibles de la capa JavaScript. Son etapas distintas. **Fuente: Construcción, p. 10.**

### Preparación

```bash
npm install --global eas-cli
eas login
eas build:configure
```

La clase sitúa `eas.json` en la raíz, junto a `package.json`, y utiliza perfiles con nombre para agrupar opciones. **Fuente: Construcción, pp. 11–12.**

```json
{
  "build": {
    "development": {
      "developmentClient": true,
      "distribution": "internal"
    },
    "preview": {
      "distribution": "internal"
    },
    "production": {}
  }
}
```

**Fuente: Construcción, p. 12.**

| Perfil del ejemplo | Resultado y uso |
| --- | --- |
| `development` | Cliente de desarrollo propio con los módulos nativos del proyecto; se conecta a Metro para probar cambios. No es la entrega de tienda. |
| `preview` | Distribución interna; en el ejemplo Android, APK que otra persona puede probar sin levantar Metro. |
| `production` | Artefacto preparado para el circuito de tienda, AAB o IPA según plataforma. |

Los nombres son convenciones del archivo, no una prohibición de crear otros perfiles. La fuente indica `production` cuando no se especifica perfil. **Fuente: Construcción, pp. 12–13.**

La elección práctica del video amplía el cuadro: **el APK que se construye sigue necesitando Metro porque se eligió `development`**. Incluir los módulos nativos propios permite probarlos, pero no convierte al cliente de desarrollo en una build de preview. Preview y production se explican como alternativas y no como resultados ejecutados en esa sesión. **Fuente: U07.T01, aproximadamente 12:20–19:55.**

### Compilar y administrar la firma

```bash
eas build --platform android --profile production
eas build:list
```

La primera compilación puede generar credenciales administradas o utilizar las existentes. Para una app ya publicada hay que considerar su continuidad de firma. En iOS, el flujo se apoya en la cuenta de desarrollador y las piezas de firma de Apple. **Fuente: Construcción, p. 14.**

El recorrido mostrado comprende subir el proyecto, generar nativo mediante prebuild, compilar con Gradle/Xcode y firmar. La tarea continúa en el servidor aunque se cierre la espera de la terminal; `build:list` consulta su estado. **Fuente: Construcción, p. 15.**

#### Proyecto de biometría: recorrido del build en la nube

La práctica utiliza **el proyecto de biometría**: iniciar sesión en Expo, **vincular el proyecto con EAS**, elegir **Android y el perfil `development`**, gestionar las credenciales e iniciar el build en la nube. Se registra la secuencia conceptual sin reconstruir respuestas de consola, identificadores o comandos que no estén en los aportes recibidos. Los comandos de production del PDF anterior conservan su atribución y **no se confunden con el perfil ejecutado en el video**. **Fuente: U07.T01, aproximadamente 19:55–36:56.**

### Distribución interna

En Android se comparte el enlace o QR de un APK instalable sin publicar en la tienda. En iOS la distribución ad hoc descrita exige registrar dispositivos y que estén contemplados por el aprovisionamiento. El comando mostrado es `eas device:create`. **Fuente: Construcción, p. 16.**

Para iOS, la fuente distingue build de simulador —que requiere una Mac para ejecutarlo—, distribución a iPhone real y App Store/TestFlight. EAS puede compilar en su infraestructura desde un proyecto trabajado en Windows o Linux; eso no elimina las condiciones de cuenta y distribución. **Fuente: Construcción, pp. 21–23.**

### Versionado

Hay dos números diferentes:

- **`version`:** versión visible que se comunica al usuario.
- **`android.versionCode` / `ios.buildNumber`:** número interno de los envíos.

La clase insiste en incrementar el número interno para evitar envíos duplicados. Muestra una configuración de EAS con fuente remota y aumento automático:

```json
{
  "cli": { "appVersionSource": "remote" },
  "build": {
    "production": { "autoIncrement": true }
  }
}
```

**Fuente: Construcción, pp. 17–18.** Este bloque amplía la configuración de perfiles; no debe sustituirla borrando opciones necesarias.

Mientras compila, el docente distingue **versión visible** de **contador interno**, con `versionCode` en Android y `buildNumber` en iOS. Se retoma esa diferencia sin repetir la configuración del PDF ni suponer que ambos números representan la misma decisión. **Fuente: U07.T01, aproximadamente 19:55–36:56.**

### Firma manual como referencia

El anexo presenta `keytool -genkeypair`, keystore, alias, RSA de 2048 bits y validez de 10.000 días. También menciona el asistente de Android Studio. Compara esa administración manual con credenciales guardadas por EAS y propone el flujo administrado para la cursada. Se conserva el concepto sin generar claves. **Fuente: Construcción, pp. 25–26.**

En clase, la firma manual se integra como **alternativa explicada**, no como una segunda firma realizada sobre el resultado de la demostración. Los cupos, precios y condiciones de cuentas que aparecen en el intercambio corresponden a ese contexto; no se registran como valores vigentes comprobados. **Fuente: U07.T01, aproximadamente 19:55–36:56.**

### Resultado comprobado y dos enlaces o QR distintos

El build **termina**, se **instala el APK** y se abre **el cliente de desarrollo**. Hay dos pasos que no deben confundirse:

- **Enlace o QR para obtener el APK:** permite descargar e instalar el artefacto del build.
- **QR para conectarse a Metro:** permite al cliente instalado cargar el proyecto desde el servidor de desarrollo.

El docente **cambia un texto de la app y muestra el cambio en pantalla**. Ese es el resultado comprobado en la sesión: una app development instalada que recibe cambios mediante Metro. No se demuestra un envío a tienda ni un despliegue OTA. **Fuente: U07.T01, 36:56–47:40.**

## 3. Activos y configuración de producción

### Ícono y splash

La fuente pide un ícono principal PNG de **1024 × 1024**, cuadrado, sin redondear sus esquinas, y muestra para Android `adaptiveIcon` con imágenes de frente, monocromática y color de fondo. Se diferencian así el ícono general y los recursos adaptativos. **Fuente: Publicación, p. 4.**

Para splash utiliza el plugin `expo-splash-screen`, con imagen, color de fondo, ancho y variante oscura. Indica probar el resultado en una compilación preview o production en lugar de inferirlo de Expo Go. **Fuente: Publicación, p. 5.**

La configuración de producción debe revisar `name`, `android.package`, `ios.bundleIdentifier`, `version` y declaraciones/textos de permisos. Los identificadores representan la identidad de la app y deben elegirse con cuidado antes de publicar. **Fuente: Publicación, p. 6.**

### Ficha y declaraciones

La publicación incluye trabajo distinto del código: nombre, descripciones, palabras clave, capturas por formato, imágenes, política de privacidad y declaraciones de contenido y datos. El material destaca que una URL de privacidad accesible forma parte de esa preparación. **Fuente: Publicación, p. 8.**

Esto se conecta con los permisos de Unidad 4 y el manejo de datos de Unidad 6: la ficha debe describir lo que la aplicación realmente solicita y utiliza, no una configuración genérica ajena al proyecto. **Fuentes: Publicación, pp. 6 y 8; Unidad 4, sección de permisos.**

T02 relaciona **ícono, splash, identificador, versión, permisos y textos de uso** con la preparación del **build de producción**. No son sustitutos de las funciones de la app: describen y configuran el artefacto que se enviará al circuito de distribución. Se conservan los detalles y ejemplos anteriores con su fuente de PDF, sin repetir perfiles, firma y formatos de T01. **Fuente: U07.T02, 02:56–12:32 y 13:52–18:24.**

## 4. Condiciones y cifras que presentan los PDF

Esta tabla registra información de las fuentes para conservar el contenido de clase. **Son datos del PDF sin validación actual**, especialmente sensibles a cambios de planes y políticas.

| Tema | Lo que afirma la presentación | Fuente |
| --- | --- | --- |
| Plan gratuito de EAS Build | 15 builds Android y 15 iOS mensuales, máximo 45 minutos por build, una concurrente y cola de baja prioridad. | Construcción, p. 19 |
| EAS Submit | Incluido sin límite de envíos en el plan que describe. | Construcción, p. 19 |
| Cuenta Google Play | 25 USD, pago único. | Publicación, p. 10 |
| Apple Developer | 99 USD por año. | Construcción, p. 21; Publicación, p. 10 |
| Dispositivos ad hoc iOS | Límite indicado de 100 por año. | Construcción, pp. 16 y 23 |
| Target Android | Exigencia descrita de API 36 desde el 31 de agosto de 2026. | Publicación, p. 7 |
| Prueba previa de Google Play | Para ciertas cuentas personales nuevas, 12 testers durante 14 días; el PDF detalla condiciones de cuenta y continuidad. | Publicación, p. 11 |
| Pruebas en tiendas | Google: interna, cerrada, abierta y producción. Apple: TestFlight interno, externo y App Store. | Publicación, p. 14 |
| Cantidades de prueba | 100 en pruebas internas; 10.000 externos en TestFlight, según el material. | Publicación, p. 14 |

La conclusión didáctica es planificar compilación y distribución con tiempo; el integrador se entrega por distribución interna, sin exigir publicación en Play. No se deduce que esos plazos hagan imposible publicar en cualquier cuatrimestre: se registra la modalidad que pide la cátedra. **Fuente: Publicación, pp. 11 y 27.**

Los costos, requisitos de SDK y cantidades de testers tratados en T02 conservan esa misma **atribución al material de la cátedra**. No se presentan como datos actuales comprobados ni se revisan aquí condiciones de cuentas reales. **Fuente: U07.T02, 02:56–12:32 y 13:52–18:24.**

## 5. EAS Submit y publicación por etapas

```bash
eas submit --platform android
eas build --platform android --auto-submit
```

La clase explica que antes se crea la aplicación en Play Console y se autorizan las credenciales de envío de EAS. Subir el archivo no completa automáticamente la ficha ni demuestra que la publicación esté aprobada. **Fuente: Publicación, p. 12.**

Para iOS muestra `ascAppId` dentro del perfil de `submit` en `eas.json` y el comando:

```bash
eas submit --platform ios
```

El identificador es el Apple ID numérico de la app en App Store Connect, no su bundle identifier. La presentación relaciona el envío con procesamiento y pruebas en TestFlight. **Fuente: Publicación, p. 13.**

Los canales permiten probar con grupos y ampliar distribución por etapas. Es distinto **subir**, **habilitar una prueba** y **publicar en producción**. El PDF enumera revisión y capacidades por modalidad, que aquí se conservan como contexto de la fuente. **Fuente: Publicación, p. 14.**

El recorrido de T02 separa **generar el binario → enviarlo con EAS Submit → distribuirlo a testers → obtener aprobación para publicarlo**. Completar una etapa no demuestra las posteriores: un archivo generado o enviado no es por sí solo una publicación aprobada. Los canales de Google Play y **TestFlight** se registran como recorridos explicados en clase. **No se demuestra una publicación efectiva** en esta sesión. **Fuente: U07.T02, 02:56–12:32 y 13:52–18:24.**

## 6. EAS Update: qué puede cambiar sin reemplazar el binario

La app compilada tiene una capa nativa y una capa de JavaScript y recursos compatibles. La primera contiene módulos, permisos y SDK; la segunda incluye componentes, textos y estilos del proyecto. Update intercambia la capa compatible sin reconstruir la parte nativa. **Fuente: Publicación, pp. 16–17.**

| La fuente permite actualizar por aire | La fuente exige nueva build |
| --- | --- |
| Correcciones de JavaScript. | Agregar o actualizar librerías nativas. |
| Textos, traducciones y estilos. | Nuevos permisos o nueva versión del SDK. |
| Reorganizar pantallas. | Ícono, splash o nombre de la app. |
| Recursos de imagen del bundle compatibles. | Cualquier cambio que necesite capacidad nativa no presente. |

**Fuente: Publicación, p. 20.** No es un mecanismo para evadir la revisión o transformar la app por fuera de las condiciones de distribución que describe la clase.

T02 propone dos casos para decidir: **corregir un texto o un error JavaScript** puede distribuirse mediante **EAS Update si el binario es compatible**; **incorporar un módulo nativo ausente** requiere **otro build**. La diferencia no depende de cuánto código se haya escrito, sino de si la app instalada dispone de la capacidad nativa necesaria. **Fuente: U07.T02, 18:24–28:08.**

### Configuración y canales

```bash
npx expo install expo-updates
eas update:configure
```

Después de preparar el mecanismo hace falta una build que lo incluya. Las actualizaciones posteriores utilizan el canal previsto:

```bash
eas update --channel production --message "Arreglo del botón de pagar"
```

**Fuente: Publicación, p. 18.** El canal conecta las builds con las actualizaciones que deben recibir. Permite separar pruebas de usuarios de producción.

### `runtimeVersion`: compatibilidad

Un canal no resuelve por sí solo si la capa nativa soporta el JavaScript nuevo. `runtimeVersion` expresa esa compatibilidad. La presentación compara versión manual, política `appVersion` y política `fingerprint`, que utiliza una huella de los factores nativos. Publicar código que espera un módulo ausente puede impedir el arranque. **Fuente: Publicación, p. 19.**

La clase distingue **dos controles**: el **canal dirige la actualización al grupo previsto** y **`runtimeVersion` identifica la compatibilidad entre JavaScript y el código nativo instalado**. El ejemplo de una app que intenta usar un módulo que su binario no contiene explica por qué no basta con enviarla al canal correcto: el destinatario también debe poder ejecutar ese cambio. Es un caso de estudio, no una prueba de despliegue OTA completada. **Fuente: U07.T02, 18:24–28:08.**

La descripción de «próximo arranque» de la p. 16 es un esquema de la clase, no una garantía de aplicación instantánea para cualquier configuración de actualización.

### Si una actualización falla

La fuente presenta lanzamiento gradual, republicar una versión anterior y rollback a la versión incluida en el binario. Son operaciones con objetivos diferentes: limitar alcance, distribuir de nuevo una versión conocida o retornar al contenido embebido. También atribuye a las diferencias de bytecode una reducción aproximada del 75 % de descarga para el entorno que describe; es una cifra del PDF, no una medición realizada aquí. **Fuente: Publicación, p. 21.**

## 7. Observar la app publicada

La app de producción corre en equipos que el desarrollador no ve. La clase distingue tres preguntas:

| Pregunta | Tipo de información | Herramientas mencionadas |
| --- | --- | --- |
| ¿Se rompe? | Errores, cierres y stack traces con contexto. | Sentry. |
| ¿La usan? | Plataformas, versiones, sesiones y recorridos. | EAS Insights, PostHog. |
| ¿Responde bien? | Arranque y tiempos de interacción reales. | EAS Observe. |

**Fuente: Publicación, p. 23.**

La integración ilustrativa de Sentry utiliza su asistente, configuración de arranque con DSN y envoltura del layout. El punto central son los **source maps**: sin relacionar el código minificado con el original, un error puede quedar reducido a posiciones poco útiles del bundle. El material diferencia la gestión de mapas en builds y después de updates. **Fuente: Publicación, p. 24.**

La analítica y los errores se relacionan con versión, canal e identificador de actualización para investigar si una falla comenzó con un envío concreto. La fuente menciona también alternativas como LogRocket, Vexo y BugSnag; no se seleccionó ni configuró ninguna. **Fuente: Publicación, p. 25.**

T02 retoma las herramientas según **qué errores ocurrieron**, **qué versiones se usan** y **cuánto tarda la app en responder**, siguiendo las preguntas del cuadro anterior. En el caso de **Sentry**, los **source maps** permiten relacionar la ubicación de un fallo en código minificado con su ubicación en el código fuente, haciendo útil el diagnóstico. La configuración es **un ejemplo explicado en clase**: no se presupone que se haya monitoreado una aplicación publicada. **Fuente: U07.T02, 28:08–31:28.**

## 8. Entrega del trabajo integrador

La modalidad indicada es una build Android preview:

```bash
eas build --platform android --profile preview
```

Se entrega el **enlace del build**, el **repositorio con `eas.json`** y una aplicación con **nombre, ícono y splash propios**. La cátedra debe poder instalarla desde Android y utilizarla sin Metro ni la computadora del grupo. No se exige publicar en Play Store. **Fuente: Publicación, p. 27.**

T02 destaca lo que recibe y prueba la cátedra: **el proyecto y un enlace descargable al APK Android generado con el perfil `preview`**. Con el comando ya documentado, el resultado esperado es un APK que puede instalarse y funcionar **sin Metro**. Se contrasta con T01, donde el APK **development** sí dependía del servidor para recibir los cambios. **Fuente: U07.T02, 00:48–02:32, 12:32–13:20 y 31:28–31:44.**

Los detalles de **`eas.json`, nombre, ícono y splash** se mantienen atribuidos al **PDF Publicación, p. 27**. La **publicación en tienda es opcional**, no un reemplazo del proyecto y la build de preview que se entregan para que la cátedra pruebe la app. No se interpreta el nombre del archivo de la grabación como evidencia de una publicación realizada. **Fuente de la orientación de entrega: U07.T02, 00:48–02:32, 12:32–13:20 y 31:28–31:44.**

Esto reúne el recorrido de la unidad: configuración, binario release, firma, distribución y validación en el contexto real de uso. El contenido de estas notas no significa que ese trabajo práctico se haya realizado ni entregado.

## Cierre y límites del material disponible

- Ambos PDF quedaron integrados con conceptos, procedimientos, comparaciones y comandos.
- No se publicaron aplicaciones ni se utilizaron cuentas de Expo, Google o Apple.
- Precios, cuotas y requisitos están atribuidos a los PDF; una decisión de publicación real requerirá verificar las condiciones aplicables.
- **2 de 2 videos incorporados:** U07.T01 – Construir la Aplicación y U07.T02 – Publicar la Aplicación. Se verificaron ambas incorporaciones, con sus dos PDF y referencias conservados.
- T01 también se identifica por el archivo «U07.T01 - Publicación de la Aplicación en la Tienda.mp4»; ambos títulos corresponden a una sola grabación, sin fecha informada, reproductor 47:43 y última marca textual 47:40.
- La demostración produce e instala un APK **development**, conectado a Metro, y muestra un cambio de texto. Preview y production se explican como alternativas; no hay subida a tienda ni despliegue OTA demostrado.
- T02 se identifica con el archivo «U07.T02 - Publicación de la Aplicación en la Tienda.mp4», sin fecha informada, reproductor **32:09** y última marca **32:08**. Amplía entrega de preview sin Metro, preparación/envío, actualización compatible y seguimiento; no demuestra publicación efectiva, despliegue OTA ni monitoreo de una app publicada.

**Documentación completa respecto del material disponible.** No quedan videos ni integraciones pendientes de Unidad 7. Los precios y políticas no verificados y los límites de las demostraciones se conservan como tales, sin bloquear el cierre.
