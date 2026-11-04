# Unidad 1 — Introducción

[Volver al índice general](00_INDICE.md)

**Estado: Documentación completa respecto del material disponible.** El usuario confirmó que no hay más material de la Unidad 1. Se integraron el programa, los PDF y los aportes recibidos de las clases del **06/08/2026** y **13/08/2026**, conservando sus límites de fuente. Los archivos de instalación no incorporados y los procedimientos no desarrollados se registran como limitaciones documentales, sin bloquear el cierre. No quedan búsquedas pendientes de videos o transcripciones para esta unidad.

## Fuentes y forma de lectura

Las referencias a PDF usan las páginas del visor, contando la portada como página 1. Las referencias a las clases usan las marcas de tiempo proporcionadas por el usuario.

| Referencia | Archivo original | Uso en esta unidad |
| --- | --- | --- |
| **Programa** | [Programa Desarrollo para móviles.docx.pdf](../fuentes/pdf/Programa%20Desarrollo%20para%20mo%CC%81viles.docx.pdf) | Alcance de la unidad, p. 3; contexto, p. 2. |
| **Enfoques** | [T01 - Enfoques de desarrollo movil.pptx.pdf](../fuentes/pdf/T01%20-%20Enfoques%20de%20desarrollo%20movil.pptx.pdf) | Presentación de 26 páginas sobre aplicaciones, enfoques y frameworks. |
| **Git** | [E01 - Git.pdf](../fuentes/pdf/E01%20-%20Git.pdf) | Presentación de 25 páginas sobre control de versiones. |
| **Campus U1** | [Curso_ A2.13 Desarrollo para Móviles _ Campus](../fuentes/pdf/Curso_%20A2.13%20Desarrollo%20para%20M%C3%B3viles%20_%20Campus) | PDF sin extensión, de 28 páginas, titulado «Unidad 1 — Introducción»; incluye enfoques, frameworks y entorno. |
| **Clase 06/08/2026** | [Video de la clase](https://www.youtube.com/watch?v=xfHmTxyB9vc) | Incorporación parcial mediante la síntesis de aportes y tiempos aproximados proporcionada por el usuario; no es una transcripción completa ni una revisión directa integral del video. |
| **Clase 13/08/2026** | «GRABACIÓN CLASE UNIDAD I - 13/08/2026». Fuente identificada por el usuario como transcripción automática; enlace no proporcionado. | Incorporación parcial a partir del listado de aportes y marcas de tiempo recibido. El usuario indica que la transcripción termina abruptamente alrededor de 1:09:24; no se registra como completa. |

Este documento organiza y explica las fuentes por tema. Las notas marcadas como **aclaración editorial** señalan diferencias o límites del material; no son contenido textual de la cátedra. Los comandos se conservan para estudiar y consultar: no se ejecutaron ni se probaron instalaciones.

**Límite de la clase del 06/08/2026:** la síntesis permite ubicar los temas y el anuncio de una posible consigna de parcial, pero no reconstruir literalmente las explicaciones, los comandos ni la demostración. Entre aproximadamente **11:00 y 22:30** se tratan organización, evaluación y defensa del proyecto; como no se conocen aquí sus condiciones exactas, no se agregan requisitos por inferencia. Las condiciones ya consignadas desde los PDF mantienen su atribución a esos documentos. Las versiones, precios y compatibilidades eventualmente mencionados en la clase no se consideran verificados actualmente.

**Límite de la clase del 13/08/2026:** el adjunto recibido contiene instrucciones de integración y una relación de aportes, no el cuerpo literal completo de la transcripción automática. Se documenta lo que ese listado respalda y se conserva el corte abrupto informado en **1:09:24**. No se reconstruyen palabras, comandos deformados, rutas locales ni opciones de pantallas ausentes. No hay enlace para esta grabación y no se le asigna el video de la clase anterior. Se normalizan los nombres de herramientas; versiones, consumos de memoria, automatismos de instalación y condiciones comerciales no se convierten en reglas actuales verificadas.

## 1. Alcance de la unidad

El programa denomina esta unidad **Introducción** y establece cuatro contenidos: enfoques de desarrollo móvil —nativos, híbridos y aplicaciones web—, frameworks de desarrollo móvil, configuración del entorno de desarrollo y Git. Campus U1 coincide con esos ejes y remite a un material separado para control de versiones. **Fuentes: Programa, p. 3; Campus U1, pp. 1–2 y 28.**

La finalidad es comprender qué implica desarrollar una aplicación móvil, comparar alternativas, reconocer las herramientas de la materia y comenzar a trabajar con control de versiones. La fundamentación del programa sitúa a React Native y Expo como tecnologías centrales de la cursada. **Fuentes: Programa, p. 2; Enfoques, p. 2; Campus U1, pp. 2 y 10.**

## 2. Qué es una aplicación móvil

Las presentaciones describen una aplicación móvil como software diseñado para instalarse en teléfonos y tablets. La distinguen de una aplicación web, utilizada desde el navegador, y destacan la posibilidad de aprovechar las capacidades del dispositivo. Entre los ejemplos aparecen la cámara, las llamadas, la ubicación y la transmisión de información mediante Bluetooth. **Fuentes: Enfoques, p. 4; Campus U1, p. 3.**

El material destaca cuatro motivos para utilizar apps:

- **Personalización:** adaptar la experiencia al usuario y al dispositivo.
- **Notificaciones:** mantener un canal de comunicación con el usuario.
- **Sensores y hardware:** utilizar cámara, GPS, Bluetooth, acelerómetro o biometría.
- **Uso sin conexión:** trabajar con datos locales; Campus U1 también menciona sincronización diferida.

**Fuentes: Enfoques, pp. 3–4; Campus U1, p. 3.**

Estas posibilidades deben evaluarse junto con el trabajo requerido: planificación, mantenimiento, pruebas en distintos dispositivos y publicación. La primera decisión del proyecto es determinar si se necesita una aplicación instalada o si una web cubre sus necesidades. **Fuentes: Enfoques, p. 4; Campus U1, p. 3.**

La clase retoma esta decisión al relacionar acceso al hardware, funcionamiento sin conexión y sincronización con la comparación entre aplicaciones móviles, web y PWA. Son aspectos que deben considerarse juntos al evaluar la alternativa, y no solo como una lista de capacidades. **Fuente: Clase 06/08/2026, aproximadamente 23:00–44:40, según la síntesis recibida.**

**Aclaración editorial para estudiar:** trabajar con datos locales y sincronizarlos son problemas distintos: conservarlos sin conexión no significa que ya se hayan intercambiado con un servidor. Esta distinción organiza los temas señalados en la síntesis; no reconstruye un mecanismo de sincronización ni un ejemplo de la demostración.

**Aclaración editorial:** Enfoques, p. 4, menciona usar el mismo código en celulares y tablets y que sea responsive. Esto no equivale a compartir código entre Android e iOS: la propia presentación explica después que el enfoque nativo mantiene código por plataforma (p. 8).

### 2.1. Cifras y contexto de la presentación

Enfoques utiliza estadísticas y proyecciones para introducir el sector. Se registran como datos de esa fuente, sin tratarlos como mediciones actuales verificadas:

| Página de Enfoques | Datos o proyecciones incluidos |
| --- | --- |
| 3 | Consumo de internet en celular equivalente al doble del escritorio; 90 % de ese consumo mediante apps; 100 mil y 30 mil nuevas apps mensuales en Google Play y Apple Store, respectivamente; más de 50 aperturas diarias de apps en la generación Z. |
| 5 | Proyección de mercado de apps de 613 mil millones de dólares para 2027; 2,17 mil millones de suscripciones 5G en 2024; previsión de IA en el 85 % de las interacciones con apps en 2025; uso de React Native por el 11 % de desarrolladores; proyección de realidad aumentada de 13,8 mil millones de dólares para 2025. |

**Aclaración editorial:** Enfoques mezcla rótulos de 2024 y 2025; Campus U1 se presenta como material de 2026. Estas cifras conservan el contexto de la presentación original. No se actualizaron ni se consultaron sus enlaces externos.

## 3. Enfoques de desarrollo móvil

Las fuentes organizan las alternativas en **nativas**, **híbridas o multiplataforma** y **web/PWA**. Cada grupo propone un equilibrio entre rendimiento, costo, acceso al dispositivo y velocidad de desarrollo. **Fuentes: Enfoques, pp. 6–7; Campus U1, pp. 4–5.**

### 3.1. Desarrollo nativo

Se crea un código fuente para cada plataforma con sus lenguajes, herramientas y entornos. Enfoques enumera Swift, Objective-C y C# en su columna de iOS, junto con Xcode; para Android enumera Java y Kotlin, junto con Android Studio. Campus U1 presenta Kotlin/Java para Android y Swift para iOS. **Fuentes: Enfoques, p. 8; Campus U1, p. 5.**

Sus ventajas son el rendimiento, el acceso directo al hardware y a las APIs del sistema, y una interfaz alineada con las guías de cada plataforma: Material Design en Android y Human Interface Guidelines en iOS. Enfoques también destaca el soporte de las comunidades de Apple y Google. **Fuentes: Enfoques, p. 9; Campus U1, p. 6.**

La contrapartida es mantener bases de código separadas, contar con perfiles especializados y afrontar mayor tiempo y costo. Las fuentes señalan también la aprobación de las tiendas como parte de las actualizaciones. Spotify y Google Maps aparecen como ejemplos del enfoque. **Fuentes: Enfoques, pp. 9 y 16; Campus U1, p. 6.**

### 3.2. Desarrollo híbrido y multiplataforma

El objetivo común es utilizar una sola base de código para varias plataformas, reutilizando conocimientos y reduciendo trabajo duplicado. Sin embargo, bajo este rótulo conviven técnicas diferentes. **Fuentes: Enfoques, pp. 10–12 y 20; Campus U1, pp. 5 y 7–8.**

#### Aplicaciones basadas en WebView

Las funcionalidades se escriben con HTML, CSS y JavaScript y se muestran en un contenedor nativo con navegador embebido: `WKWebView` en iOS y `WebView` en Android. Los ejemplos son Apache Cordova e Ionic con Capacitor. Sus plugins permiten extender las capacidades disponibles más allá de lo que ofrece el navegador. **Fuentes: Enfoques, p. 10; Campus U1, p. 7.**

#### Otras soluciones multiplataforma

React Native se presenta como una alternativa cuyos componentes se corresponden con vistas nativas de Android e iOS, sin una WebView para dibujar la interfaz. Enfoques ilustra esta relación mediante un campo de texto y pantallas equivalentes en ambas plataformas. **Fuentes: Enfoques, pp. 10–11 y 15; Campus U1, pp. 7 y 14.**

Campus U1 explica que Flutter dibuja su propia interfaz con un motor de renderizado y que Kotlin Multiplatform permite compartir lógica y conservar interfaces nativas o compartirlas mediante Compose Multiplatform. Compartir código no implica que todos los frameworks construyan la interfaz de igual manera. **Fuente: Campus U1, p. 13.**

#### Ventajas y límites

Las ventajas señaladas son una base común, menor tiempo y costo, aprovechamiento de conocimientos web y rapidez de prototipado. Algunas herramientas permiten ciertos tipos de actualización sin pasar por las tiendas; Campus U1 aclara que existen límites. **Fuentes: Enfoques, p. 12; Campus U1, p. 8.**

Entre las limitaciones figuran la dependencia del framework y sus versiones, la necesidad de plugins o integraciones para determinadas APIs, el tamaño de la app y los casos con gráficos o procesamiento intensivo. La WebView y los componentes nativos no deben evaluarse como si fueran la misma técnica. **Fuentes: Enfoques, p. 12; Campus U1, pp. 7–8 y 14.**

**Aclaración editorial:** Enfoques atribuye sobrecarga al «puente de JavaScript» (pp. 12 y 24) y habla de transformación de componentes «en tiempo de build» (pp. 10–11). Campus U1 describe la correspondencia con vistas nativas y advierte que el modelo del puente es material que la cursada considera retirado (pp. 14 y 27). Se señala la diferencia sin desarrollar arquitectura interna, que el campus remite a la Unidad 2 (p. 28).

### 3.3. Web y aplicaciones web progresivas (PWA)

Se presentan como sitios optimizados para móviles que funcionan en el navegador y pueden incorporar uso sin conexión, notificaciones e instalación. El acceso mediante URL evita exigir una instalación para comenzar a utilizarlas. **Fuentes: Enfoques, p. 13; Campus U1, pp. 5 y 9.**

Sus ventajas son las tecnologías web estándar, el costo bajo, el funcionamiento en dispositivos con navegador y las actualizaciones inmediatas sin aprobación de tiendas. Sus límites son el acceso al hardware, el rendimiento en apps complejas y las diferencias de experiencia entre navegadores y dispositivos. Las fuentes también señalan menor visibilidad respecto de las tiendas. **Fuentes: Enfoques, pp. 13 y 16; Campus U1, p. 9.**

### 3.4. Comparación y elección

| Criterio | Nativo | Híbrido / multiplataforma | Web / PWA |
| --- | --- | --- | --- |
| Código | Una base por plataforma. | Base compartida entre plataformas. | Tecnologías web en navegador. |
| Costo y tiempo | Mayores por el trabajo separado. | Menores por reutilización. | Bajos según el material. |
| Interfaz | Específica de cada plataforma. | Depende del framework: WebView, vistas nativas o renderizado propio. | Depende del navegador y del dispositivo. |
| Acceso al dispositivo | Directo a las APIs de la plataforma. | Depende del framework, sus módulos y plugins. | Más restringido. |
| Actualizaciones | Intervienen las tiendas. | Tiendas y, en ciertos casos, actualización sin tienda. | Actualización web inmediata. |
| Ejemplos citados | Spotify, Google Maps. | Instagram, Uber. | Twitter Lite, Starbucks. |

**Fuentes: Enfoques, pp. 8–16; Campus U1, pp. 5–9 y 13.** Los ejemplos conservan la clasificación de la presentación; no constituyen una auditoría de la implementación actual de esas aplicaciones.

Campus U1 propone decidir según las necesidades del proyecto:

- **Máxima exigencia de gráficos o hardware**, como juegos, realidad aumentada o edición de video: nativo.
- **Android e iOS con equipo y presupuesto acotados:** multiplataforma.
- **Contenido y formularios sin hardware específico:** web/PWA.
- **Equipo con conocimientos web y necesidad de salir rápido:** multiplataforma.

La materia elige React Native y Expo por la relación entre conocimientos web previos y una interfaz nativa. **Fuente: Campus U1, p. 10.**

#### Orientación para estudiar a partir de la clase

La comparación entre enfoques nativo, multiplataforma y web se retoma con ventajas, limitaciones y criterios de elección. **Fuente: Clase 06/08/2026, aproximadamente 44:50–1:02:45, según la síntesis recibida.**

Alrededor de **1:01:45**, el docente plantea como **posibilidad para el parcial** presentar un caso y pedir elegir y justificar un enfoque de desarrollo según las necesidades y los recursos disponibles. Es una posibilidad anunciada en esa clase, no una consigna confirmada ni una descripción completa del examen. **Fuente: Clase 06/08/2026, aproximadamente 1:01:45, según la síntesis recibida.**

**Orientación editorial de estudio:** practicar la justificación con los criterios ya desarrollados: plataformas destinatarias, hardware requerido, uso sin conexión, rendimiento, conocimientos del equipo, tiempo y presupuesto. La finalidad es explicar por qué una alternativa responde al caso; esta guía de repaso no agrega condiciones de evaluación de la cátedra.

#### Introducción a actualizaciones OTA

La síntesis identifica en este bloque una introducción a las actualizaciones **OTA** o por aire. Se vincula con la posibilidad, ya mencionada en los PDF, de actualizar determinados contenidos sin distribuir de nuevo todo el binario. Se conserva el límite entre cambios de JavaScript y cambios nativos explicado en la sección de entorno: una OTA no debe entenderse como solución para cualquier modificación de la app. **Fuentes: Clase 06/08/2026, aproximadamente 44:50–1:02:45, según la síntesis recibida; Enfoques, p. 12; Campus U1, pp. 8 y 23.** No se añade un procedimiento de publicación OTA a partir de este anuncio introductorio.

## 4. Frameworks y librerías

### 4.1. Qué aporta un framework

Un **framework** o marco de trabajo reúne herramientas, bibliotecas, patrones y convenciones para organizar el desarrollo. Propone una estructura dentro de la cual se construye la aplicación. **Fuente: Enfoques, p. 17.**

El material enumera seis aportes: organización de carpetas, archivos y clases; componentes reutilizables; patrones que favorecen consistencia y mantenimiento; automatización de tareas repetitivas; productividad al concentrarse en la lógica propia; y colaboración mediante convenciones compartidas. Como ejemplos generales menciona datos, seguridad, autenticación, sesiones y bases de datos. Son ejemplos del papel de un framework, no una lista de prestaciones obligatorias de todos ellos. **Fuente: Enfoques, p. 18.**

### 4.2. Diferencia con una librería

Una **librería** ofrece código reutilizable para tareas específicas. El desarrollador decide cuándo invocarlo y cómo integrarlo. Un **framework** controla parte del flujo y de la estructura; se trabaja siguiendo sus reglas. La diferencia se denomina **inversión de control**. **Fuentes: Enfoques, p. 19; Campus U1, p. 12.**

| Aspecto | Librería | Framework |
| --- | --- | --- |
| Flujo | El código de la aplicación llama a la librería. | El framework establece el flujo y las convenciones. |
| Integración | Se incorpora a la estructura elegida por el desarrollador. | Se construye dentro de su estructura. |
| Ejemplos del material | Lodash, date-fns. | React Native, NestJS, Next.js, Angular. |

Enfoques utiliza React Native como ejemplo de reglas para renderizar componentes y manejar estado. Campus U1 compara resolver controles con librerías sueltas con utilizar piezas ya integradas, como un guard de NestJS o un middleware de Next.js. El ejemplo ilustra la inversión de control; no se desarrollan aquí esas herramientas. **Fuentes: Enfoques, p. 19; Campus U1, p. 12.**

## 5. Frameworks de desarrollo móvil del material

La clase presenta React Native con Expo, Flutter, Kotlin Multiplatform e Ionic con Capacitor. Se integra esa referencia al panorama comparativo desarrollado a continuación, sin duplicar sus definiciones ni atribuir a la clase características que la síntesis no detalla. **Fuente: Clase 06/08/2026, aproximadamente 1:02:50–1:07:20, según la síntesis recibida.**

### 5.1. React Native y Expo

Enfoques presenta React Native como un framework de código abierto desarrollado por Facebook que permite construir aplicaciones para Android e iOS con JavaScript y React, una base de código y una arquitectura de componentes. Campus U1 menciona también TypeScript y describe la correspondencia con vistas nativas. **Fuentes: Enfoques, p. 21; Campus U1, pp. 13–14.**

**React Native y Expo cumplen papeles distintos.** React Native es el framework de la interfaz; Expo aporta SDK, CLI y servicios para facilitar el desarrollo, la compilación y la publicación. El SDK permite acceder a capacidades del dispositivo; los servicios en la nube evitan depender de disponer localmente de todas las herramientas nativas para compilar. **Fuentes: Enfoques, p. 21; Campus U1, pp. 13–14 y 21.**

Las ventajas destacadas son rendimiento cercano al nativo, recarga rápida al guardar, reutilización de conocimientos de React y un ecosistema amplio de comunidad y paquetes npm. Como límites se mencionan el tamaño de la app y la necesidad de módulos personalizados o config plugins para integraciones específicas. Campus U1 cita Instagram, Discord, Shopify y Coinbase como ejemplos. **Fuentes: Enfoques, p. 21; Campus U1, p. 14.**

#### Ejemplo de correspondencia de componentes

Enfoques muestra este fragmento junto a un `EditText` de Android y un campo de texto para iOS:

```jsx
<TextInput
  style={styles.input}
  onChangeText={onChangeNumber}
  value={number}
  placeholder="useless placeholder"
  keyboardType="numeric"
/>
```

**Fuente: Enfoques, p. 11, captura de código.** Es un fragmento ilustrativo: no incluye las definiciones de `styles`, `onChangeNumber` y `number` ni un proyecto completo. Muestra la relación conceptual con controles de las plataformas; no implica que el código nativo de la diapositiva sea una traducción literal de ese fragmento.

### 5.2. Ionic y Capacitor

**Ionic** se describe como una herramienta de interfaz de código abierto basada en HTML, CSS y JavaScript, integrable con Angular, Vue o React. La presentación indica que surgió en 2013 en Drifty Co. y originalmente se construyó sobre AngularJS y Apache Cordova. **Fuente: Enfoques, p. 22.**

**Capacitor** aporta SDK, CLI, plugins de interacción con el dispositivo y una API para crearlos. La combinación permite empaquetar la interfaz web en WebViews nativas. **Fuentes: Enfoques, pp. 10 y 22; Campus U1, p. 13.**

Resulta familiar para equipos web y reutiliza sus flujos de trabajo. Las limitaciones señaladas son el rendimiento condicionado por la WebView, la dependencia de sus actualizaciones y una interfaz menos cercana a la nativa que la de React Native. **Fuentes: Enfoques, p. 23; Campus U1, p. 13.**

### 5.3. Flutter

Flutter es un framework de código abierto de Google que utiliza **Dart** y permite desarrollar para móviles, web, escritorio y dispositivos integrados con una base de código. Enfoques presenta su compilación a código de máquina y su interfaz basada en widgets. Campus U1 destaca que dibuja su interfaz con un motor de renderizado, en vez de usar los componentes visuales del sistema. **Fuentes: Enfoques, pp. 24–25; Campus U1, p. 13.**

Enfoques enumera widgets personalizables, componentes Material Design y Cupertino, Hot Reload, soporte multiplataforma y paquetes de Pub.dev. Menciona plugins para cámara, GPS y notificaciones, y paquetes para Firebase y animaciones. Identifica Skia como motor gráfico en su explicación; se conserva la atribución al material, sin convertirla en una descripción actual verificada de todas las versiones y plataformas. **Fuente: Enfoques, pp. 24–25.**

### 5.4. Kotlin Multiplatform

Campus U1 incorpora **Kotlin Multiplatform**, de JetBrains, como alternativa para compartir lógica de negocio entre plataformas y mantener interfaces nativas o compartirlas con Compose Multiplatform. **Fuente: Campus U1, p. 13.**

**Aclaración editorial:** la p. 7 de Campus U1 agrupa React Native, Flutter y Kotlin Multiplatform bajo «componentes nativos reales», pero la p. 13 distingue renderizado propio en Flutter y opciones de interfaz en Kotlin Multiplatform. Para compararlos se conservan esas descripciones específicas, sin suponer que generan la interfaz de igual forma.

### 5.5. Mención exploratoria: widgets y Live Activities

Campus U1 presenta `expo-widgets` para escribir widgets de pantalla de inicio y Live Activities de iOS en TypeScript con componentes de Expo UI. Aclara que es solo para iOS, queda fuera de Expo Go y **no se utilizará en la materia**. Ilustra que una parte de la app puede verse en la pantalla de inicio o bloqueo sin abrirla y que el sistema decide cuándo actualizarla. Es una mención de la fuente, no una configuración requerida. **Fuente: Campus U1, p. 15.**

## 6. Entorno de desarrollo con Expo

Esta sección integra Campus U1, cuya portada identifica Expo SDK 57, React Native 0.86 y React 19.2. Son las versiones declaradas por la presentación, no una selección comprobada durante la elaboración de estos apuntes. **Fuente: Campus U1, p. 1.**

### 6.1. Preparación inicial

Para comenzar con Expo Go, el material pide:

1. **Node.js LTS**, que incluye npm y npx.
2. **Un editor**, proponiendo VS Code con ESLint y Prettier.
3. **Un teléfono con Expo Go**, instalado desde la tienda.

Para este primer recorrido no exige Android Studio, Xcode, JDK ni variables de entorno. Distingue la preparación mínima de la instalación completa para emulación y compilación local. **Fuente: Campus U1, p. 17.**

La apertura de la clase distingue React Native y Expo del editor y de las herramientas para ejecutar o probar el proyecto; presenta Expo Go como alternativa al uso de un emulador. **Fuente: Clase 06/08/2026, aproximadamente 00:00–10:20, según la síntesis recibida.**

**Aclaración editorial apoyada en los PDF:** el editor es donde se escribe el código; React Native es el framework con el que se construye la aplicación; Expo aporta herramientas y servicios, y Expo Go permite probarla en el teléfono. Son funciones diferentes, aunque se utilicen juntas. Expo Go no reemplaza al editor ni equivale al framework. **Fuentes de esta organización: Campus U1, pp. 14 y 17–19.**

#### Herramientas y preparación nativa: ampliación del 13/08/2026

La clase amplía la distinción entre empezar con Expo Go y preparar una máquina para compilación nativa y depuración. La segunda preparación agrega herramientas de construcción y comunicación con Android; no convierte a Android Studio en un requisito para el primer recorrido con Expo Go. **Fuentes: Clase 13/08/2026, 00:53–16:36, según los aportes recibidos; Campus U1, pp. 17 y 25.**

| Herramienta | Función para comprender el entorno |
| --- | --- |
| Node.js | Ejecutar las herramientas JavaScript del proyecto en la computadora de desarrollo. |
| Gestor de paquetes | Instalar y administrar dependencias; el PDF presenta npm junto con Node.js. |
| Editor | Escribir y revisar el código; no sustituye al framework ni al emulador. |
| Chocolatey | Herramienta mencionada para gestionar instalaciones en Windows. |
| nvm | Herramienta mencionada para administrar versiones de Node.js. |
| JDK | Herramientas Java que participan en la preparación de compilación Android. |
| Android SDK | Conjunto de herramientas y plataformas de desarrollo Android. |
| Android Studio | Entorno que reúne herramientas para trabajar con Android, incluido Device Manager. |
| ADB | Comunicación con dispositivos o emuladores para tareas de desarrollo y diagnóstico. |
| Platform Tools | Herramientas de la plataforma entre las que se encuentra ADB. |
| Build Tools | Herramientas utilizadas para construir los artefactos Android. |
| Gradle | Sistema que coordina el proceso de construcción y sus tareas. |

**Fuentes: Clase 13/08/2026, 00:53–16:36, según los aportes recibidos; Campus U1, pp. 17 y 25 para la preparación mínima y completa.** La tabla organiza las funciones para estudiar; no prescribe versiones, un orden universal de instalación ni el uso obligatorio de Chocolatey o nvm. No se reconstruyen sus comandos.

### 6.2. Crear y ejecutar el proyecto

```bash
npx create-expo-app@latest mi-app
cd mi-app
npx expo start
```

La secuencia crea el proyecto, entra en su carpeta e inicia el servidor de desarrollo. Se escanea el QR con la cámara en iOS o desde Expo Go en Android. El teléfono y la computadora deben estar en la misma red. Si la red aísla los dispositivos, la presentación propone:

```bash
npx expo start --tunnel
```

**Fuente: Campus U1, p. 18.**

La clase recorre la preparación del entorno, la creación y ejecución de un proyecto y su conexión con Expo Go. Los comandos anteriores siguen atribuidos al PDF: la síntesis audiovisual no permite reconstruir una secuencia adicional ni los detalles exactos de lo que se ejecutó. **Fuente: Clase 06/08/2026, aproximadamente 1:07:25–1:18:40, según la síntesis recibida.**

#### Primer recorrido por el proyecto

Entre aproximadamente **1:18:40 y 1:25:30**, la clase recorre `app.json`, recursos, rutas, componentes, constantes y hooks. Este primer reconocimiento del proyecto conecta la configuración con los archivos que componen la aplicación. **Fuente: Clase 06/08/2026, según la síntesis recibida.**

**Alcance de esta incorporación:** la síntesis no especifica un árbol completo de carpetas, nombres de archivos de la demostración ni modificaciones concretas. Se registra el recorrido sin inventarlos ni convertir esta introducción en un desarrollo de rutas o hooks que corresponda a otras unidades.

### 6.3. Expo Go y sus límites

Expo Go es una aplicación contenedora que carga el proyecto sin compilar una aplicación propia. Permite ver cambios al guardar y comenzar sin configuración nativa. Se propone para aprender fundamentos e iterar rápidamente. **Fuente: Campus U1, p. 19.**

El límite aparece al necesitar código nativo que no está incluido en ese contenedor. Campus U1 señala como situaciones para pasar a un **development build** una librería nativa no disponible, un config plugin que cambie la configuración nativa, cambios de permisos, ícono o nombre y la prueba de la app tal como llegará al usuario. **Fuente: Campus U1, p. 20.**

La clase también trata las limitaciones de las librerías disponibles en Expo Go dentro del recorrido de creación y ejecución. Se integra como refuerzo de esta distinción, sin agregar una lista de compatibilidades no incluida en la síntesis. **Fuente: Clase 06/08/2026, aproximadamente 1:07:25–1:18:40, según la síntesis recibida.**

**Aclaración editorial:** la p. 20 agrupa cámara, ubicación, sensores y notificaciones como capacidades del SDK utilizables con Expo Go, pero no precisa versiones ni condiciones. Esa enumeración orientativa no demuestra que cualquier función o configuración de esos módulos funcione en cualquier Expo Go. Su tratamiento específico no forma parte de esta introducción.

### 6.4. Development build y compilación en la nube

Un **development build** es una compilación propia de la app con herramientas de desarrollo y las librerías nativas del proyecto. Se instala y luego se continúa trabajando con el servidor de desarrollo. **Fuente: Campus U1, p. 21.**

La secuencia de la presentación es:

```bash
npx expo install expo-dev-client
npm install --global eas-cli
eas login
eas build --platform android --profile development
npx expo start
```

**Fuente: Campus U1, p. 21.** Se separaron la instalación de EAS CLI y el inicio de sesión, que aparecen unidos con `&&` en la diapositiva.

El flujo agrega el cliente de desarrollo, instala EAS CLI, inicia sesión y solicita una compilación Android en la nube. Antes del último comando, la fuente indica instalar la compilación en el dispositivo. Explica también que la nube permite generar una versión de iOS desde Windows o Linux. **Fuente: Campus U1, p. 21.**

**Aclaración editorial:** la diapositiva utiliza el perfil `development`, pero no explica cómo configurarlo ni todos los pasos de instalación del resultado. Es un esquema de clase, no una guía completa validada desde cero.

### 6.5. Tres formas de compilar

| Forma | Comando del material | Requisitos y uso señalados |
| --- | --- | --- |
| En la nube | `eas build` | Cuenta de Expo; no exige herramientas nativas locales. Permite compilar para iOS sin Mac. |
| Local con EAS | `eas build --local` | Herramientas nativas instaladas; evita usar el cupo de compilaciones en la nube. |
| Local sin EAS | `npx expo run:android` / `npx expo run:ios` | Entorno nativo local: Android Studio o Xcode en macOS. Iteración sobre código nativo. |

**Fuentes: Campus U1, pp. 22–23.** La fuente menciona un cupo mensual del plan gratuito de EAS, sin cantidades; tampoco detalla compatibilidad por sistema operativo de `--local`.

El cierre de la clase introduce development builds y la elección entre compilación local y en la nube. La síntesis permite registrar esa introducción, pero no completar comandos, configuraciones, costos o condiciones de las alternativas. **Fuente: Clase 06/08/2026, aproximadamente 1:25:35–1:29:25, según la síntesis recibida.**

Para compilar localmente muestra:

```bash
npx expo run:android
npx expo run:ios
npx expo run:android --device
```

El segundo corresponde a iOS en macOS; el tercero permite elegir dispositivo o emulador. La presentación explica que este flujo genera carpetas nativas mediante `prebuild`, compila e instala. **Fuente: Campus U1, p. 23.**

La distinción práctica es entre **cambios nativos**, que requieren compilar —agregar una librería nativa o cambiar un config plugin—, y **cambios en JavaScript o TypeScript**, para los que se continúa con `npx expo start`. Metro sirve el código actualizado sin repetir la compilación nativa. **Fuente: Campus U1, p. 23.**

### 6.6. Debug y release: distinción introductoria

Campus U1 diferencia compilaciones **debug**, con Metro, recarga y herramientas de desarrollo, de **release**, con JavaScript empaquetado en la app y sin herramientas de desarrollo. Para estas últimas menciona minificación y bytecode de Hermes. **Fuente: Campus U1, p. 24.**

```bash
npx expo run:android --variant release
npx expo run:ios --configuration Release
```

**Fuente: Campus U1, p. 24.** Se presentan como pruebas locales. La fuente remite firma y publicación a otra unidad; aquí solo se conserva la distinción necesaria para comprender el entorno.

### 6.7. Emulación, simulación y diagnóstico

Para el entorno completo se mencionan Android Studio con SDK y Device Manager, JDK 17 y `ANDROID_HOME`; para iOS, Xcode y su simulador en macOS. El material favorece probar en teléfono real para apreciar tiempos, gestos y tamaños. Remite el paso a paso a `entorno.html`, que no está entre las fuentes incorporadas. **Fuentes: Campus U1, pp. 17 y 25.**

Para diagnóstico e instalación compatible de paquetes muestra:

```bash
npx expo-doctor
npx expo install <paquete>
```

El primero revisa versiones, dependencias y configuración. El segundo permite que Expo seleccione la versión compatible con el SDK. `<paquete>` debe reemplazarse por el nombre correspondiente. **Fuente: Campus U1, p. 26.**

Diagnóstico e instalación de dependencias compatibles también aparecen en el cierre audiovisual. Los comandos de esta sección proceden del PDF local; no se agregan otros a partir de la síntesis. La ampliación del entorno en la clase **no equivale a haber leído `entorno.html`**, archivo que no forma parte de las fuentes disponibles; esta limitación no bloquea el cierre de la documentación. **Fuente: Clase 06/08/2026, aproximadamente 1:25:35–1:29:25, según la síntesis recibida.**

#### Crear y probar un emulador Android

La clase del 13/08/2026 presenta este recorrido general:

1. Abrir **Device Manager** y crear un dispositivo virtual.
2. Elegir el dispositivo que se quiere representar y una imagen del sistema.
3. Configurar sus recursos e iniciar el emulador.
4. Probar cambios de orientación, condiciones de señal y ubicación o rutas simuladas.
5. Si no inicia, revisar la disponibilidad y configuración de virtualización.

**Fuente: Clase 13/08/2026, 16:36–23:13, según los aportes recibidos.** No se agregan nombres de opciones de pantalla, cantidades de RAM, imágenes concretas ni ajustes que el texto recibido no describe. La simulación permite explorar situaciones de uso; no demuestra por sí sola el comportamiento en todo teléfono real.

#### Conectar un teléfono Android por USB

El recorrido explicado permite usar el dispositivo físico en tareas de desarrollo:

1. Localizar el **número de compilación** y usarlo para activar las opciones de desarrollador.
2. Habilitar **depuración USB**.
3. Conectar el teléfono a la computadora y aceptar en el dispositivo la autorización de esa computadora.
4. Comprobar si aparece con el comando:

```bash
adb devices
```

**Fuente: Clase 13/08/2026, 23:23–26:56, según los aportes recibidos.** La ubicación y los nombres de los menús varían según fabricante. Este procedimiento no implica que todo dispositivo quede autorizado automáticamente al conectar el cable.

#### iOS y herramientas adicionales

La clase menciona **Xcode y el simulador en macOS** y **Expo Orbit** como herramienta adicional. Para el caso de una computadora Windows y un iPhone, indica probar mediante Expo Go. Esto describe el recorrido de prueba tratado en esa clase, no elimina las diferencias entre probar con Expo Go y compilar una aplicación propia. **Fuentes: Clase 13/08/2026, 27:05–35:16, según los aportes recibidos; Campus U1, pp. 21 y 25.** No se añaden pasos de instalación de Orbit ni operaciones que no estén descritas.

#### Diagnóstico del entorno y variables

| Síntoma o situación tratada | Qué revisar según la ampliación de clase |
| --- | --- |
| Comando no reconocido | Instalación de la herramienta y disponibilidad mediante `PATH`. |
| SDK no encontrado | Instalación del SDK y configuración de sus referencias de entorno. |
| Dudas sobre `ANDROID_HOME` | Distinguir el SDK de la instalación del editor Android Studio y comprobar la ubicación efectiva antes de configurar. |
| Emulador que no inicia | Virtualización y preparación del entorno del emulador. |
| Teléfono no detectado | Depuración USB, conexión, autorización y detección con ADB. |

**Fuente: Clase 13/08/2026, 27:05–35:16, según los aportes recibidos; virtualización también en 16:36–23:13.** El listado es una orientación de diagnóstico, no una garantía de una causa única por síntoma.

**Inconsistencia y contraste editorial:** el aporte recibido advierte que la explicación de `ANDROID_HOME` la asocia tanto al SDK como a la instalación de Android Studio. Campus U1, p. 25, distingue Android Studio, el SDK que utiliza y la variable, pero no proporciona una ruta de instalación ni una instrucción detallada para fijarla. Por eso no se equiparan ambas carpetas ni se inventa un valor para la variable. Para configurar un equipo debe comprobarse la ubicación de su SDK; los archivos de instalación no incorporados limitan el detalle de estas instrucciones, sin constituir un pendiente de cierre.

### 6.8. Uso de agentes de IA según la cátedra

Campus U1 menciona Expo MCP Server y Expo Skills para dar al agente acceso a documentación y procedimientos de Expo. Incluye este ejemplo de configuración para Claude:

```bash
claude mcp add --transport http expo https://mcp.expo.dev/mcp
```

**Fuente: Campus U1, p. 27.** Se registra como ejemplo; no se ejecutó ni se configuraron servicios.

La advertencia docente es que un agente puede proponer APIs o modelos antiguos con seguridad. La regla expresada permite utilizarlo, pero exige explicar cada línea del código entregado; el parcial y la defensa del integrador se realizan sin agente. **Fuente: Campus U1, p. 27.**

## 7. Control de versiones y Git

**Nota de ubicación:** la portada de Git dice «Unidad 2 - Control de versiones & GIT» (p. 1). Se integra aquí porque el programa ubica Git en la Unidad 1 y Campus U1 identifica el deck como complementario de esta misma unidad. **Fuentes: Programa, p. 3; Campus U1, pp. 2 y 28.**

### 7.1. Para qué sirve

Cuando varias personas modifican un proyecto, pueden cambiar los mismos lugares y producir problemas de integración. El control de versiones permite mantener un historial, recuperar versiones anteriores, trabajar en líneas independientes e identificar cada cambio mediante un mensaje. **Fuente: Git, pp. 2–3.**

El material distingue sistemas **centralizados**, con el repositorio de referencia en un servidor, y **descentralizados**, donde cada computadora dispone de archivos e historial clonados. Git pertenece al segundo grupo. Se presenta como herramienta de código abierto creada por Linus Torvalds, con operaciones locales rápidas y posibilidad de alojar repositorios privados o utilizar GitHub, GitLab o Bitbucket. **Fuente: Git, pp. 4–6.**

La clase distingue **Git**, herramienta de control de versiones, de **GitHub, GitLab y Bitbucket**, plataformas donde pueden alojarse repositorios y organizarse colaboración. Utilizar Git localmente no equivale a haber subido el proyecto a una de ellas. Se incorpora esta diferencia sin repetir los comandos del PDF; el tramo no desarrolla remotos ni `push`. **Fuente: Clase 13/08/2026, 50:08–53:46, según los aportes recibidos.**

### 7.2. Instalación e identidad

La presentación propone descargar Git del sitio oficial, seguir el instalador y configurar nombre y correo. Enumera clientes gráficos como GitHub Desktop o Sourcetree, extensiones de IDE y línea de comandos como formas de uso. **Fuente: Git, p. 7.**

```bash
git config --global user.email "email@example.com"
git config --global user.name "username"
```

Los valores de ejemplo identifican al autor que aparecerá en los commits. **Fuentes: Git, pp. 7 y 14.**

### 7.3. Repositorio, working tree y staging

Se inicializa el repositorio con `git init` dentro de la carpeta del proyecto. La captura muestra cómo indicar una rama inicial:

```bash
git init --initial-branch=nombre_rama
```

`nombre_rama` se reemplaza por el nombre elegido; la captura recomienda `main`. Se crea `.git`, que contiene información del repositorio: hooks, información del proyecto, objetos con las versiones y referencias que relacionan nombres con commits. **Fuente: Git, p. 8.**

| Lugar | Qué representa |
| --- | --- |
| **Working tree / working directory** | Archivos tal como se están editando, incluidos los seguidos por Git y los nuevos sin seguimiento. |
| **Staging area / área intermedia** | Cambios preparados para incluir en el próximo commit. |
| **Repositorio** | Historial de snapshots confirmados mediante commits. |

**Fuentes: Git, pp. 8–11.**

El flujo es **editar → preparar con `git add` → confirmar con `git commit`**. Preparar un archivo todavía no crea un commit: staging y repositorio son lugares distintos. **Fuentes: Git, pp. 10–11.**

### 7.4. Primer archivo y primer commit

```bash
git add <archivo.ext>
git add -A
git commit -m "Descripción detallada pero breve de lo que se hizo"
git status
```

**Fuentes: Git, pp. 10–11, capturas.** Las formas de `add` son alternativas: preparar un archivo o agregar todos los cambios. El nombre entre `< >` se reemplaza por la ruta correspondiente.

Un **commit** registra una instantánea del proyecto. Después de confirmar, el material consulta `git status` y muestra un working tree limpio. **Fuente: Git, p. 11.**

### 7.5. Mensajes e historial

Un mensaje útil permite comprender propósito y contexto, colaborar y localizar errores. La presentación recomienda claridad, concisión y un título de una línea. Si se necesita más información, `git commit` abre un editor para escribir título y cuerpo. También recomienda imperativo. **Fuente: Git, pp. 12–13.**

**Aclaración editorial:** aunque recomienda imperativo, los ejemplos de la p. 13 emplean formas como «Arreglé» y «Se arregló». Se conserva la recomendación señalando la inconsistencia de los ejemplos.

```bash
git log
```

El historial muestra el **hash** identificador, autor, fecha y hora, y mensaje del commit. **Fuente: Git, p. 14.**

### 7.6. Ramas

Una **rama** representa una línea de desarrollo independiente para implementar funciones, corregir errores o experimentar antes de integrar. El material también menciona ramas estables para releases y hotfixes que eviten arrastrar trabajo todavía en curso. **Fuente: Git, p. 15.**

```bash
git branch
git branch <nombre-rama>
git checkout <nombre-rama>
git checkout -b <nombre-rama>
git branch <nombre-rama> -D
```

En orden: listar ramas, crear una, cambiar a ella, crear y cambiar en una operación y eliminarla con la opción `-D` mostrada en la captura. **Fuente: Git, p. 16.**

El equipo puede acordar nombres como `feat/<funcionalidad>`, `fix/<funcionalidad-a-arreglar>` y `hotfix/<funcionalidad-a-arreglar>`. La convención comunica el propósito de la rama. **Fuente: Git, p. 16.**

### 7.7. Integración y tipos de merge

El **merge** integra cambios de una rama en otra. La presentación utiliza `main` y `nueva-rama` e indica ubicarse en la rama que recibirá los cambios:

```bash
git checkout main
git merge nueva-rama
```

**Fuentes: Git, pp. 16–17.**

- **Fast-forward:** las historias no han divergido; la rama a integrar contiene los commits de la principal y cambios posteriores.
- **Three-way merge:** las ramas divergieron. Se comparan el ancestro común más reciente, el último commit de la rama actual y el último de la rama entrante. Si los cambios son compatibles, Git integra automáticamente; de lo contrario marca conflictos.

**Fuente: Git, p. 18.**

### 7.8. Conflictos

Un conflicto aparece cuando Git no puede integrar automáticamente. El ejemplo modifica la misma función de suma: una rama suma tres argumentos y la otra recibe un arreglo y utiliza `reduce`. **Fuentes: Git, pp. 19–20.**

La captura muestra este bloque conflictivo; el cierre de la función queda fuera del bloque:

```text
<<<<<<< HEAD
function suma(a, b, c){
  return a + b + c;
=======
function suma(array) {
  return array.reduce((acumulador, actual) => acumulador + actual, 0);
>>>>>>> feat/sum-array
```

- `<<<<<<< HEAD` inicia los cambios de la rama actual.
- `=======` separa las alternativas.
- `>>>>>>> feat/sum-array` cierra la sección de la rama entrante.

**Fuente: Git, p. 20, captura y explicación.**

Se resuelve editando el archivo para conservar el cambio deseado y eliminando los marcadores y el contenido descartado. Luego se prepara y confirma:

```bash
git add <nombre-archivo>
git commit -m "fix: conflictos de integracion"
```

El ejemplo final conserva la versión que suma los elementos del arreglo. **Fuente: Git, p. 21.**

### 7.9. Restaurar, revertir y guardar temporalmente

| Necesidad | Comando | Efecto explicado por la fuente | Página de Git |
| --- | --- | --- | --- |
| Descartar cambios de un archivo en el working tree | `git restore <archivo>` | Restaura el contenido desde la versión de referencia del staging, según el esquema. | 22 |
| Retirar cambios del próximo commit | `git restore --staged <archivo>` | Modifica staging y conserva la edición en el working tree. | 23 |
| Restaurar staging y working tree | `git restore --staged --worktree <archivo>` | Restaura ambas áreas. | 23 |
| Deshacer un commit mediante otro | `git revert HEAD` o `git revert <HASH_COMMIT>` | Crea un nuevo commit que revierte los cambios seleccionados. | 24 |
| Apartar trabajo sin commit | `git stash` | Guarda temporalmente los cambios para retomar después. | 25 |
| Incluir archivos nuevos sin seguimiento | `git stash -u` | Incluye esos archivos en el guardado temporal. | 25 |
| Recuperar lo guardado | `git stash pop` | Retoma los cambios apartados. | 25 |

`HEAD` se presenta como referencia al último commit de la rama actual y `HASH_COMMIT` como identificador del commit. Quitar del staging conserva la edición del archivo; restaurar el working tree descarta esa edición. `revert`, en cambio, registra el deshacer en el historial. **Fuentes: Git, pp. 22–25.**

**Corrección editorial de transcripción:** las capturas de Git, p. 23, escriben `git restor`. Se utiliza `git restore`, como aparece en el esquema de esa misma página y en la p. 22.

## 8. Ejemplo de aplicación y orientaciones del trabajo práctico

### 8.1. Aplicación de visitas a clientes

La clase presenta una app para gestionar visitas a clientes, con listado y detalle alimentados por datos simulados (**mocks**). El recorrido relaciona ubicación, mapas, llamadas, registro de visita, notas y fotografías, como capacidades que permiten construir un caso de uso móvil. También introduce **geocodificación**, es decir, pasar de una dirección a coordenadas. **Fuente: Clase 13/08/2026, 35:23–45:58, según los aportes recibidos.**

Para estudiar el ejemplo hay que separar sus niveles:

- **Demostración y recorrido de funcionalidades:** clientes con mocks y uso o presentación de las capacidades anteriores. El listado recibido no permite reconstruir el código ni afirmar que cada operación esté integrada de extremo a extremo.
- **Objetivos proyectados, todavía no implementados en esa demostración:** almacenamiento sin conexión y sincronización.
- **Posibilidad adicional mencionada:** Stripe; no se registra como requisito del trabajo ni como integración desarrollada.

**Fuente: Clase 13/08/2026, 35:23–45:58, según los aportes recibidos.** El ejemplo complementa la discusión de hardware y uso offline de la sección 2, sin demostrar que la persistencia y la sincronización ya estuvieran resueltas.

### 8.2. Anuncios sobre el trabajo práctico

En esa fecha se plantean casos de uso cuyos requisitos se ampliarían progresivamente y la posibilidad de continuar una idea previa, previa consulta con los docentes. La orientación es cubrir los contenidos de la materia. También se contempla reutilizar una API anterior después de revisar su adecuación. **Fuente: Clase 13/08/2026, 46:21–49:50 y 54:02–54:45, según los aportes recibidos.**

La intención docente de proporcionar APIs y utilizar PostgreSQL se registra como **anuncio de esa clase**. La alternativa no relacional permanece tentativa. No se afirma que esas APIs se hayan entregado ni que exista aquí una consigna definitiva con requisitos, fechas o condiciones adicionales. **Fuente: Clase 13/08/2026, 46:21–49:50 y 54:02–54:45, según los aportes recibidos.**

### 8.3. Adelanto para una futura integración en Unidad 2

Entre **54:54 y 1:09:24**, el material anticipa TypeScript, React, props, estado, listas, hooks, ciclo de vida y testing. Se identifica el tramo para una integración posterior en Unidad 2, sin desarrollar nuevamente esos temas aquí ni modificar ahora su archivo. **Fuente: Clase 13/08/2026, según los aportes recibidos; final abrupto informado alrededor de 1:09:24.**

**Aclaración editorial:** las simplificaciones del adelanto no implican que el tipado elimine todos los errores ni que existan solo dos clases de pruebas. Tampoco se considera cubierta la clase específica sobre arquitectura de React Native y Expo, tema remitido a Unidad 2 y que no condiciona el cierre de Unidad 1.

## 9. Cierre y limitaciones de las fuentes disponibles

Campus U1 indica como práctica **crear el proyecto y subirlo al repositorio del grupo** (p. 28). Git desarrolla el flujo local, pero no incluye una secuencia para configurar un remoto y subir el proyecto. Se registra esa ausencia como limitación de las fuentes disponibles, sin reconstruir el procedimiento ni bloquear el cierre.

La síntesis de la clase del 06/08/2026 señala que la **subida al repositorio** y la **arquitectura de React Native y Expo** se anuncian para la clase siguiente. No se consideran desarrolladas por ese anuncio; no se dispone de una marca de tiempo específica para esos anuncios en el listado recibido.

La incorporación del 13/08/2026 amplía el entorno y diferencia Git de sus plataformas, pero **no desarrolla remotos ni subida** y **no cubre la clase de arquitectura**. Estas delimitaciones se conservan como tales: no implican buscar más material de Unidad 1, cuya disponibilidad fue confirmada por el usuario.

| Material o aspecto | Estado |
| --- | --- |
| Alcance del programa | Verificado: Programa, p. 3. |
| Enfoques, comparaciones y frameworks | Integrados desde Enfoques y Campus U1. |
| Preparación inicial y panorama del entorno | Integrados desde Campus U1, pp. 17–27. |
| Control de versiones y Git | Integrado, incluidas las capturas de comandos. |
| Clase del 06/08/2026 | Síntesis de aportes incorporada parcialmente por tema, con tiempos aproximados y sin transcripción completa. |
| Clase del 13/08/2026 | Aportes integrados por tema desde el listado recibido, referido a una transcripción automática cortada alrededor de 1:09:24. Sin enlace ni cuerpo literal completo disponible aquí. |
| Instalación completa del entorno | Ampliado con la clase del 13/08/2026; entorno.html y tutorial de instalación mencionado en clase no incorporados como archivos. Limitación de las fuentes, sin bloquear el cierre. |
| Otros materiales audiovisuales | El usuario confirma que no hay más material de Unidad 1. No quedan búsquedas pendientes de videos ni transcripciones. |
| Subida inicial al repositorio del grupo | Anunciada para la clase siguiente; procedimiento no desarrollado en la síntesis ni en las fuentes locales leídas. |
| Arquitectura de React Native y Expo | Anunciada, sin desarrollo en los aportes recibidos; remitida a Unidad 2, sin bloquear el cierre de Unidad 1 ni incorporarla por inferencia. |
| Organización, evaluación y defensa en la clase | Bloque aproximado 11:00–22:30 identificado, pero sin condiciones exactas disponibles; no se completan por inferencia. |
| Orientaciones del TP del 13/08/2026 | Anuncios registrados con sus límites; no equivalen a consigna definitiva ni recursos entregados. |
| Adelanto de Unidad 2 del 13/08/2026 | Tramo 54:54–1:09:24 identificado para futura integración en esa unidad; no sustituye la clase de arquitectura ni condiciona el cierre de Unidad 1. |

La Unidad 1 queda cerrada como **Documentación completa respecto del material disponible**. Esto no convierte en completas las fuentes recibidas: se conserva, en particular, la aclaración de que la transcripción automática del 13/08/2026 termina abruptamente alrededor de **1:09:24**. Las limitaciones registradas no generan tareas de búsqueda ni bloquean el cierre.
