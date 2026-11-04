# Unidad 6 — Computación ubicua, IoT y seguridad

[Volver al índice](00_INDICE.md)

**Estado: unidad abierta. 2 grabaciones incorporadas: Computación ubicua e IoT y Seguridad.** Se conservan los dos PDF y los aportes anteriores, y se amplían por tema las secciones de seguridad con la segunda grabación. Todavía no se confirmó cuántos videos tiene la Unidad 6: no se establece un total ni una cantidad de grabaciones faltantes.

## Fuentes y alcance

| Referencia | Fuente original | Páginas |
| --- | --- | --- |
| **IoT** | [Unidad 6 — Computación ubicua e IoT · Desarrollo para Móviles.pdf](../fuentes/pdf/Unidad%206%20%E2%80%94%20Computaci%C3%B3n%20ubicua%20e%20IoT%20%C2%B7%20Desarrollo%20para%20M%C3%B3viles.pdf) | 19 |
| **Seguridad** | [Unidad 6 — Seguridad · Desarrollo para Móviles.pdf](../fuentes/pdf/Unidad%206%20%E2%80%94%20Seguridad%20%C2%B7%20Desarrollo%20para%20M%C3%B3viles.pdf) | 30 |

El programa, p. 3, incluye almacenamiento seguro, tokens, biometría, computación ubicua, capas, campos de aplicación e Internet de las cosas. Los apuntes integran también autenticación, contenido web y comunicación porque forman parte de los PDF. Las páginas son las del visor, incluida la portada. Las indicaciones se documentan como material de la cátedra, sin auditoría de una app ni verificación externa de versiones, estándares o servicios. Los fragmentos no se ejecutaron.

**Fuente audiovisual:** [GRABACIÓN UNIDAD 6 - COMPUTACIÓN UBICUA E IOT](https://campus.uner.edu.ar/fcad/mod/url/view.php?id=56301), sin fecha de grabación informada. La última marca de transcripción indicada por el usuario es **27:46**; no se deduce de ella una duración distinta ni contenido posterior.

**Alcance de la incorporación:** se utilizan los aportes y tiempos recibidos en el pedido, no una revisión directa ni el cuerpo literal completo de los subtítulos. El enlace del campus no fue accesible desde la herramienta disponible. Las referencias **Grabación IoT** identifican estos aportes; los contenidos específicos de seguridad mantienen la atribución al PDF **Seguridad**, sin presentarlos como desarrollados en esta grabación.

**Segunda fuente audiovisual:** «GRABACIÓN UNIDAD 6 - SEGURIDAD», archivo identificado como **`UNIDAD 6 - SEGURIDAD.mp4`**. Duración indicada: **42:03**; última marca de transcripción: **41:58**. No se proporcionaron fecha ni enlace; el enlace de IoT corresponde exclusivamente a la primera grabación. Las referencias **Grabación Seguridad** atribuyen los aportes y tiempos recibidos para esta segunda fuente, sin afirmar una revisión directa del archivo ni una transcripción literal íntegra. Las referencias al PDF Seguridad se conservan por separado.

## 1. Computación ubicua

La idea atribuida a Mark Weiser en 1991 es que el cómputo se integra a la vida cotidiana hasta dejar de percibirse como una computadora separada. La presentación lo ejemplifica con SUBE, molinetes, semáforos, terminales de pago y termostatos. **Fuente: IoT, p. 4.**

Sus características son:

- **Invisible:** el usuario no necesita reconocer una computadora o una pantalla para que exista procesamiento.
- **Contextual:** responde a la ubicación, actividad o situación.
- **Distribuida:** participan muchos dispositivos en lugar de un único equipo central visible.

**Fuente: IoT, p. 4.**

La clase utiliza **pagar con tarjeta** y **viajar con SUBE** para mostrar el cómputo integrado en una actividad cotidiana: la persona realiza una compra o un viaje sin pensar cada paso como una interacción con una computadora. El procesamiento forma parte de la actividad, aunque no se presente como una computadora de propósito general. No se reconstruye desde esos ejemplos la arquitectura técnica de los sistemas de pago o transporte. **Fuente: Grabación IoT, 00:14–08:09, según los aportes recibidos.**

### Escalas y ambientes inteligentes

El material presenta tres escalas: **dust**, dispositivos muy pequeños como etiquetas RFID y sensores; **skin**, superficies y materiales que reaccionan; y **clay**, objetos con volumen con los que se interactúa físicamente. La finalidad de la clasificación es reconocer interfaces que no dependen de teclado; el teléfono puede ocupar el papel de interfaz del conjunto. **Fuente: IoT, p. 5.**

Los ambientes inteligentes integran sensores y procesamiento en el espacio. Los ejemplos son iluminación por presencia, climatización que aprende horarios y riego según humedad del suelo. La comodidad de actuar sin un pedido explícito plantea privacidad: se generan datos sobre personas que no necesariamente iniciaron una interacción. **Fuente: IoT, p. 6.**

La grabación retoma **dust, skin y clay** dentro de esa clasificación: dispositivos pequeños, superficies que reaccionan y objetos físicos con volumen son formas distintas de integrar cómputo. No son nombres de protocolos ni capas del sistema IoT. En el riego, además, deben distinguirse **el sensor que mide humedad** y **el actuador que abre el agua**: medir informa sobre el entorno; actuar lo modifica. **Fuentes: Grabación IoT, 00:14–08:09; IoT, pp. 5–6.**

## 2. Internet de las cosas

IoT se define como objetos físicos con sensores, cómputo y conexión que recopilan y comparten datos con poca intervención humana. La fuente lo relaciona con chips de bajo costo y consumo, sensores pequeños, conectividad y procesamiento en la nube. **Fuente: IoT, p. 8.**

Entre los campos de aplicación aparecen pulseras de salud, sensores de humedad y temperatura del agro, detección de desgaste industrial y contenedores urbanos que informan su llenado. El teléfono deja de ser todo el producto: pasa a ser parte de un sistema mayor. **Fuente: IoT, pp. 2 y 8.**

### Arquitectura por capas

| Capa | Función |
| --- | --- |
| Percepción | Sensores que captan el mundo físico y actuadores que lo modifican. |
| Red | Transporte por Wi-Fi, Bluetooth, LoRa o red celular. |
| Middleware | Normalización, integración y almacenamiento de datos heterogéneos. |
| Aplicación | Interfaz y funciones para el usuario; aquí participa la app móvil. |
| Negocio | Analítica, decisiones y modelo del producto. |

**Fuente: IoT, p. 9.** El middleware desacopla a la app de si un dispositivo utiliza MQTT, CoAP o HTTP. La app recibe una interfaz de datos más uniforme.

La clase recorre estas capas con **el ejemplo agrícola**: el **sensor toma una lectura**, la **red la transporta**, el **middleware normaliza los datos** y la **app permite consultarlos y decidir si hace falta regar**. La secuencia vincula las responsabilidades del cuadro con una necesidad concreta, sin convertir la pantalla móvil en responsable de todas las capas ni atribuir una implementación completa al ejemplo explicado. **Fuente: Grabación IoT, 08:09–17:11.**

### Direccionamiento y retos

La presentación contrasta IPv4, con direcciones de 32 bits y unos 4.300 millones de valores, con IPv6, de 128 bits y aproximadamente `3,4 × 10^38`. Menciona simplificación de cabeceras, autoconfiguración y descubrimiento local, e IPsec como parte de su diseño. **Fuente: IoT, p. 10.**

**Aclaración editorial:** la mención de IPsec no demuestra que un sistema esté protegido automáticamente por utilizar IPv6; la diapositiva no desarrolla una configuración de seguridad de red.

Los cuatro retos son **fiabilidad** —no perder información crítica sin advertirlo—, **rendimiento** —responder dentro del tiempo útil—, **interoperabilidad** —integrar fabricantes y protocolos— y **seguridad/privacidad** —dispositivos mantenibles y datos que revelan hábitos o presencia—. **Fuente: IoT, p. 11.**

El caso agrícola permite separar **una lectura incorrecta** de **una alerta correcta que llega demasiado tarde**. La primera pone en duda el dato sobre el que se decide; la segunda puede perder utilidad aunque su contenido sea correcto. Revisar el valor no sustituye revisar el tiempo de respuesta del conjunto. **Fuente: Grabación IoT, 08:09–17:11.**

Para privacidad, la clase utiliza **el historial de encendido de luces**: puede revelar cuándo hay alguien en casa. No hace falta que el dato se llame «presencia» para permitir deducirla. Este ejemplo amplía el reto del cuadro; se conserva la precisión anterior de que IPv6 y la mención de IPsec no acreditan por sí solos una configuración de seguridad efectiva. **Fuente: Grabación IoT, 08:09–17:11; contraste: IoT, pp. 10–11.**

## 3. La app dentro de un sistema IoT

### Conexión directa o por nube

| Directa | Mediante plataforma |
| --- | --- |
| Teléfono ↔ dispositivo por BLE, Wi-Fi local o NFC. | Teléfono ↔ API o WebSocket del middleware ↔ dispositivo. |
| Apropiada para elementos cercanos como pulseras, balanzas o cerraduras. | Apropiada para acceso remoto, como ver información de casa desde otro lugar. |
| Requiere proximidad según la tecnología. | Requiere conectividad en los extremos. |

El ejemplo combina BLE para la primera configuración de un aparato y nube para el uso cotidiano. **Fuente: IoT, p. 13.**

La grabación contrasta **una pulsera, balanza o cerradura cercana** con **consultar las luces desde el trabajo**. En el primer caso interesa la conexión próxima al dispositivo; en el segundo se necesita acceso remoto al sistema. El patrón combinado utiliza **BLE para la configuración inicial** y **una plataforma en línea para el acceso remoto cuando el caso lo requiere**. No se lo convierte en obligación para todo objeto conectado. **Fuente: Grabación IoT, aproximadamente 17:11–20:30.**

### BLE desde Expo

La presentación utiliza `react-native-ble-plx`, que requiere código nativo, config plugin y development build. No se prueba dentro de Expo Go. **Fuente: IoT, p. 14.**

```ts
import { BleManager } from 'react-native-ble-plx';

const manager = new BleManager();
manager.startDeviceScan(null, null, (error, device) => {
  if (error) return;
  if (device?.name === 'MiSensor') {
    manager.stopDeviceScan();
    device.connect()
      .then(d => d.discoverAllServicesAndCharacteristics())
      .then(leerTemperatura);
  }
});
```

**Fuente: IoT, p. 14.** El fragmento muestra descubrir, detener el escaneo, conectar y descubrir servicios antes de leer. `leerTemperatura` no está implementada en el PDF; no se inventan servicios, UUID ni formato del dato.

La clase destaca permisos de Bluetooth que dependen de la versión de Android, posible necesidad de ubicación en equipos anteriores, desconexiones, batería y reconexión. Requiere hardware real; menciona ESP32 como ejemplo de dispositivo de prueba. El escaneo también puede revelar ubicación indirectamente por los dispositivos cercanos. **Fuente: IoT, p. 15.**

**Aclaración editorial:** el ejemplo es introductorio y no incorpora todos los permisos, tratamiento de errores, limpieza del administrador o reconexión que la misma fuente identifica como necesarios.

El relato de clase se vincula con el fragmento del PDF: **iniciar el escaneo → identificar el dispositivo → detener el escaneo → conectar**. La necesidad de un **development build** corresponde al módulo nativo, y los permisos se revisan según la versión de Android. También se contempla perder conexión por **distancia o batería**, por lo que encontrar un dispositivo una vez no garantiza que siga disponible. **Fuente: Grabación IoT, aproximadamente 20:30–23:05.**

El docente explica por qué hace falta **hardware real para probar BLE**. Se registra como recorrido explicado: **la grabación no documenta una prueba física exitosa** de escaneo, conexión y lectura. Los auxiliares y servicios no detallados siguen siendo límites del fragmento del PDF, no resultados completados por esta incorporación. **Fuente: Grabación IoT, aproximadamente 20:30–23:05.**

### Una plataforma IoT

ThingsBoard se presenta como middleware de código abierto para recibir telemetría por MQTT, HTTP o CoAP, almacenarla, administrar dispositivos, definir reglas y exponer una API REST. Una regla ilustrativa es avisar al superar 30 °C. **Fuente: IoT, p. 16.**

La clase explica el recorrido de **ThingsBoard** como plataforma que **recibe y almacena telemetría** y la expone mediante una **API REST**. La app puede consultarla con **`fetch` o Axios**, reutilizando el trabajo de redes de Unidad 5, en lugar de necesitar conocer directamente el protocolo de cada sensor. No se atribuye a la grabación una conexión ejecutada a una instalación concreta ni un despliegue verificado. **Fuente: Grabación IoT, 23:14–27:46.**

```tsx
const { data } = useQuery({
  queryKey: ['telemetria', dispositivoId],
  queryFn: async () => {
    const r = await fetch(
      `${BASE}/api/plugins/telemetry/DEVICE/${dispositivoId}/values/timeseries`,
      { headers: { 'X-Authorization': `Bearer ${token}` } },
    );
    return r.json();
  },
  refetchInterval: 5000,
});
```

**Fuente: IoT, p. 17, normalizando espacios de la extracción.** La app vuelve a utilizar la lógica de redes y caché de la Unidad 5. `BASE`, `token` e identificador son datos externos al fragmento. **Diferencia entre materiales:** este ejemplo no comprueba `r.ok`, mientras Redes, p. 6, lo exige para diferenciar errores HTTP. Debe leerse como demostración del recorrido, no como manejo completo de fallos.

El teléfono aporta **interfaz**, **sensores propios** y **canal de notificación**. Así se recombinan las capacidades estudiadas en las unidades anteriores. **Fuente: IoT, p. 18.**

La grabación retoma esas tres funciones: el celular permite **consultar y configurar**, puede **aportar datos de sus propios sensores** y **recibir avisos**. Son papeles dentro del sistema explicado, no prueba de que todas esas integraciones estén implementadas en una app de la clase. Los temas específicos de seguridad que siguen continúan basados en el PDF Seguridad. **Fuente: Grabación IoT, 23:14–27:46.**

## 4. Modelo de exposición de una app móvil

La seguridad parte de que el binario y su bundle pueden quedar en manos de quien quiera inspeccionarlos. La fuente menciona lectura de cadenas, proxies y dispositivos modificados. Ofuscar no equivale a cifrar ni convierte una clave integrada en un secreto. **Fuente: Seguridad, p. 4.**

También influyen redes fuera del control del desarrollador, acceso a sensores sensibles, pérdida física del teléfono y demora de distribución de parches. Las variables de entorno que terminan incluidas en el bundle no resuelven ese problema. **Fuente: Seguridad, pp. 4–5.**

**Aclaración editorial:** la advertencia sobre no incorporar secretos de servidor debe distinguirse de almacenar después del login un token del usuario en el almacén seguro del dispositivo, caso que la propia clase desarrolla.

La grabación relaciona esa exposición con decisiones concretas: **el paquete instalado puede inspeccionarse**, el teléfono puede perderse y la aplicación puede utilizar redes ajenas. Una **clave privada del servidor no debe quedar dentro del bundle**, aunque se haya incorporado desde una variable de entorno: cambiar el origen de la cadena no evita que termine distribuida con la app. Se distingue ese secreto de servidor del token de sesión que el usuario obtiene al ingresar y que requiere almacenamiento local adecuado. **Fuente: Grabación Seguridad, aproximadamente 00:04–13:47.**

## 5. Riesgos OWASP que utiliza la presentación

La fuente usa **OWASP Mobile Top 10, edición 2024**, como mapa de riesgos y advierte sobre la numeración diferente de la edición 2016. Se transcribe su clasificación como contenido del PDF, no como comprobación de cuál sea la edición vigente al consultar estos apuntes. **Fuente: Seguridad, pp. 7–8.**

| Código | Riesgo según la presentación |
| --- | --- |
| M1 | Uso indebido de credenciales. |
| M2 | Cadena de suministro insegura. |
| M3 | Autenticación/autorización insegura. |
| M4 | Validación de entrada y salida insuficiente. |
| M5 | Comunicación insegura. |
| M6 | Controles de privacidad insuficientes. |
| M7 | Protección del binario insuficiente. |
| M8 | Configuración de seguridad incorrecta. |
| M9 | Almacenamiento de datos inseguro. |
| M10 | Criptografía insuficiente. |

Para los trabajos de la materia enfatiza credenciales, dependencias, autenticación y comunicación. Como ejemplos menciona claves dentro del código, paquetes comprometidos o abandonados, sesiones sin expiración, autorización decidida en el cliente y HTTP sin protección. `npm audit` aparece como herramienta de revisión de dependencias, no como prueba de seguridad completa. **Fuente: Seguridad, p. 9.**

La clase vincula esos ejemplos con la tabla anterior: **credenciales** implica decidir qué no se distribuye y dónde se guarda el token; **dependencias**, revisar lo que se incorpora; **autorización**, no confiar solamente en lo que habilita una pantalla del cliente; y **comunicación**, proteger el intercambio con el servidor. **`npm audit` revisa dependencias frente a vulnerabilidades conocidas**; no demuestra que un proyecto quede libre de todos los riesgos de la tabla. **Fuente: Grabación Seguridad, aproximadamente 00:04–13:47; relación con Seguridad, pp. 8–9.**

## 6. Almacenamiento seguro y tokens

### Preferencias frente a credenciales

`kv-store` sirve para preferencias, pero la fuente indica que no está cifrado. Para tokens y credenciales utiliza `expo-secure-store`, apoyado en mecanismos del sistema: Keystore en Android y Keychain en iOS. **Fuente: Seguridad, pp. 11–12.**

```ts
import * as SecureStore from 'expo-secure-store';

await SecureStore.setItemAsync('token', valor);
const token = await SecureStore.getItemAsync('token');
await SecureStore.deleteItemAsync('token');
```

Solo almacena texto; los objetos requieren serialización. La lectura puede devolver `null`. No es una base para grandes volúmenes y los errores por tamaños o condiciones de plataforma deben manejarse. **Fuente: Seguridad, pp. 12–13.**

La clase describe diferencias de persistencia al desinstalar en Android e iOS, pero advierte que conservar datos de Keychain tras reinstalar no es una garantía sobre la que diseñar. También importa explicar al usuario qué ocurre con sus datos. **Fuente: Seguridad, p. 13.**

El ejemplo de la grabación contrasta **la preferencia de tema**, que puede ir en un almacén de preferencias, con **el token de sesión**, que corresponde proteger con `expo-secure-store`. El recorrido de guardar, leer y borrar se relaciona con los tres métodos del fragmento anterior, sin repetirlo. Si leer devuelve **`null`**, no hay un token disponible bajo esa clave para recuperar la sesión: no se lo trata como credencial válida. La app debe poder **pedir un nuevo ingreso tras una reinstalación**, sin depender de que el almacenamiento haya sobrevivido. **Fuente: Grabación Seguridad, aproximadamente 13:47–19:35; contraste: Seguridad, pp. 11–13.**

### Access token y refresh token

| Access token | Refresh token |
| --- | --- |
| Vida corta. | Vida más larga. |
| Se adjunta a requests autorizados. | Permite obtener nuevos access tokens. |
| Su expiración limita temporalmente una filtración. | Su exposición puede permitir prolongar una sesión. |

La fuente indica SecureStore para ambos y que cerrar sesión exige borrarlos localmente y revocar el refresh token en el servidor. El borrado del teléfono no invalida por sí solo una credencial ya copiada. **Fuente: Seguridad, p. 14.**

La grabación refuerza el alcance distinto de los tokens: el **access token de vida corta** autoriza las solicitudes y el **refresh token permite renovarlo**. Por eso el cierre de sesión conecta **borrado local y revocación del refresh token en el servidor**; borrar solamente la copia del dispositivo no invalida otra copia que se hubiera obtenido. La tabla y la referencia del PDF anteriores mantienen su atribución. **Fuente: Grabación Seguridad, aproximadamente 13:47–19:35; Seguridad, p. 14.**

## 7. Biometría

`expo-local-authentication` permite consultar hardware, comprobar si hay datos biométricos registrados e iniciar autenticación local. El resultado se revisa mediante `success`; debe existir una alternativa ante falta de lector, fallo o cancelación. **Fuente: Seguridad, p. 15.**

```ts
const hayLector = await LocalAuthentication.hasHardwareAsync();
const hayHuellas = await LocalAuthentication.isEnrolledAsync();
if (hayLector && hayHuellas) {
  const r = await LocalAuthentication.authenticateAsync({
    promptMessage: 'Confirmá tu identidad',
    cancelLabel: 'Cancelar',
  });
  if (r.success) abrirSesion();
}
```

**Fuente: Seguridad, p. 15.** Es un control local, no una implementación completa de sesión de servidor.

La clase distingue mostrar un diálogo de proteger el acceso al dato. Con `requireAuthentication: true`, SecureStore condiciona la lectura a autenticación. Advierte que cambios biométricos pueden invalidar la clave y que ese flujo requiere configuración y development build según las condiciones descritas. **Fuente: Seguridad, p. 16.**

```ts
await SecureStore.setItemAsync('refresh_token', valor, {
  requireAuthentication: true,
  authenticationPrompt: 'Desbloqueá para continuar',
});
```

**Fuente: Seguridad, p. 16.**

La clase distingue dos operaciones: **mostrar el diálogo con `expo-local-authentication`** y **exigir autenticación para leer un token de SecureStore mediante `requireAuthentication`**. Las comprobaciones de hardware y biometría registrada permiten decidir si ofrecer ese camino; ante cancelación o fallo debe existir una alternativa. Una respuesta biométrica local favorable **no crea por sí sola una sesión válida en el servidor**. Los dos fragmentos anteriores ilustran funciones distintas y no sustituyen un flujo completo de sesión. **Fuente: Grabación Seguridad, aproximadamente 19:35–23:15.**

## 8. Login delegado, OAuth y PKCE

El material propone que el usuario se autentique en el proveedor mediante el navegador del sistema, conservando visible su dominio. La app recibe el resultado de autorización sin tener que capturar la contraseña del proveedor. **Fuente: Seguridad, p. 18.**

El flujo de código de autorización se explica en cinco pasos: abrir el proveedor, autenticación y consentimiento, retorno de un código, canje por token y almacenamiento seguro. **Fuente: Seguridad, p. 19.**

PKCE agrega un **verifier** aleatorio y un desafío derivado que se envía al comenzar. Al canjear el código se necesita el verifier original; interceptar solo el código no alcanza para completar ese canje. El PDF indica que `expo-auth-session` lo activa por defecto. **Fuente: Seguridad, p. 20.**

La muestra de código utiliza `useAuthRequest`, endpoints de autorización/token, `makeRedirectUri({ scheme: 'tuapp' })` y `promptAsync()`. También incluye `WebBrowser.maybeCompleteAuthSession()` y deshabilita el botón hasta que exista `request`. La fuente exige development build para el esquema propio. **Fuente: Seguridad, pp. 21–22.**

**Aclaración editorial:** la p. 21 combina endpoints de GitHub con un scope de ejemplo y no implementa el procesamiento de la respuesta ni todo el canje. No constituye una integración completa con ese proveedor. Se documentan los pasos sin inventar credenciales, scopes válidos o configuración ausente.

Cuando el proveedor exige `client_secret`, el canje que lo utiliza se coloca en un backend; el secreto no se incorpora a la aplicación. **Fuente: Seguridad, p. 23.** La navegación protegida del cliente no sustituye la autorización que debe aplicar ese servidor.

El recorrido del proveedor explicado en clase es **abrir el navegador del sistema → reconocer el dominio → autenticarse → volver a la app con un código → canjearlo**. El **challenge** se relaciona con el **verifier** que deberá presentarse en el canje: quien intercepta solamente el código no tiene todo lo necesario para completarlo. El **manejo del canje en el backend** se atribuye al diseño explicado en esa clase, sin presentarlo como código desplegado ni imponerlo como descripción única de cualquier integración OAuth. **Fuente: Grabación Seguridad, aproximadamente 23:15–33:55.**

Este **login delegado** se diferencia del **login con usuario y contraseña previsto en el integrador**: ilustra otra manera de obtener autorización del proveedor y no cambia por sí mismo la consigna del proyecto. Se conserva la distinción entre el flujo conceptual y las limitaciones del ejemplo de código del PDF. **Fuente: Grabación Seguridad, aproximadamente 23:15–33:55; contexto de integrador documentado en Unidad 2.**

## 9. Contenido web, navegador y HTTPS

Una WebView permite incrustar contenido existente, como términos o reportes, pero introduce riesgos de contenido no confiable, redirecciones y pérdida de la barra de dominio. El material propone limitar orígenes, bloquear destinos ajenos y desactivar capacidades no utilizadas. Para login utiliza el navegador del sistema; para contenido externo lo propone como opción preferente. **Fuente: Seguridad, pp. 25–27.**

La grabación utiliza el ejemplo de **una pantalla de ingreso que imita al proveedor**: si no hay una dirección visible, al usuario le cuesta comprobar dónde escribe la contraseña. Para contenido embebido, el criterio es **restringir la navegación a los orígenes previstos**, sin considerar confiable cualquier destino solo por verse dentro de la app. Esto se vincula con la observación técnica del fragmento de WebView que sigue, no la elimina. **Fuente: Grabación Seguridad, 33:55–41:58.**

**Observación editorial sobre el ejemplo de WebView:** Seguridad, p. 26, usa `req.url.startsWith('https://midominio.edu.ar')`. Ese prefijo no demuestra que el hostname sea exactamente el permitido: también coincide con texto que continúe el nombre de dominio. Por eso el fragmento no se presenta como un control exhaustivo de orígenes. La intención de restringir destinos y el detalle concreto de la implementación deben distinguirse.

Para abrir contenido en navegador, la presentación muestra:

```ts
await WebBrowser.openBrowserAsync('https://uner.edu.ar');
```

**Fuente: Seguridad, p. 27.**

La comunicación se plantea sobre HTTPS. La clase introduce certificate pinning como una restricción adicional de confianza y explica su costo ante rotación de certificados; no lo pide para el integrador. No incluye una configuración de pinning ni un procedimiento de despliegue. **Fuente: Seguridad, p. 28.**

Cada módulo debe solicitar solo el permiso necesario, en el momento oportuno; el PDF advierte sobre ejemplos antiguos de `expo-permissions`. Esto relaciona seguridad con minimización de datos y experiencia de uso. **Fuente: Seguridad, p. 29.**

La clase retoma **HTTPS** para la comunicación y el pedido de permisos **al usar la función correspondiente**. El contexto de la acción ayuda a explicar por qué se solicita el acceso; no se da por hecho que el usuario lo concederá. El flujo de declaración, solicitud y rechazo ya está desarrollado en [Unidad 4](04_UNIDAD_4.md), por lo que no se duplica aquí. **Fuente: Grabación Seguridad, 33:55–41:58.**

## Cobertura y revisión posterior

- Ambos PDF quedaron integrados: conceptos, capas y aplicaciones de IoT; acceso directo/nube; riesgos, almacenamiento, tokens, biometría, autenticación y contenido web.
- Los ejemplos BLE, plataforma IoT y OAuth no contienen todos los componentes de un sistema real; sus auxiliares y configuraciones ausentes no se inventaron.
- Se señalaron límites concretos de los fragmentos y diferencias con otras fuentes.
- **2 grabaciones incorporadas:** **Computación ubicua e IoT**, última marca informada **27:46**, y **Seguridad**, duración indicada **42:03** y última marca **41:58**. Ninguna tiene fecha de grabación proporcionada; Seguridad no tiene enlace y no utiliza el de IoT.
- **Cantidad total de videos de Unidad 6: no confirmada.** No se supone un denominador ni una cantidad faltante. La unidad permanece abierta.
- La grabación amplía las secciones 1 a 3 con ejemplos cotidianos, riego y capas, privacidad de las luces, conexiones cercanas/remotas, BLE y ThingsBoard. No documenta una prueba física exitosa de BLE; los contenidos específicos de seguridad conservan su atribución al PDF Seguridad.
- La **Grabación Seguridad** amplía las secciones 4 a 9 con decisiones de exposición, OWASP, sesión y almacenamiento, biometría, OAuth/PKCE, WebView, HTTPS y permisos. Se conservan las tablas, ejemplos y referencias de los PDF sin duplicarlos ni dar por implementados los recorridos explicados.
