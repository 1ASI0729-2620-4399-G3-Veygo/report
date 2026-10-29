# Capítulo V: Product Implementation, Validation & Deployment.

## 5.1. Software Configuration Management.

Software Configuration Management (SCM), es un conjunto de actividades y procesos que tiene como objetivo organizar y supervisar los cambios que se realizan en el software durante su desarrollo, usaremos esto para garantizar que nuestro producto se mantenga consistente, funcional y confiable, a medida que evoluciona con el tiempo. 

### 5.1.1. Software Development Environment Configuration.

En esta sección pasamos a referenciar los productos de software que usamos como equipo para colaborar en la realización de este proyecto, considerando actividades como Project Management, Requirement Management, Product UX/UI Design, Software Development, Software Testing y Software Documentation.


<h4>Project Management: </h4>

Los productos de software que usamos aquí, nos ayudó como equipo a gestionar tareas, tiempos, recursos y comunicación.

- **Whatsapp:** Es una aplicación de mensajería ampliamente utilizada para la comunicación rápida y eficaz. Permite a los usuarios compartir mensajes de texto, fotos, videos, enlaces, videollamadas y documentos. Usamos sus funciones para mantenernos en contacto a través de un grupo privado donde coordinamos avances, compartimos archivos y enlaces. Además, establecíamos fechas límite y organizamos el cumplimiento de metas mediante una comunicación constante, lo que permitió un mejor seguimiento del progreso del equipo.

- **Discord:** Es una aplicación de mensajería que permite comunicarse mediante canales de voz y texto. La utilizamos para realizar reuniones cortas y aclarar dudas en tiempo real mediante llamadas de voz. También aprovechamos su función de recordatorios y notificaciones para mantener un control adecuado del tiempo y asegurar el cumplimiento de las tareas asignadas.

<h4>Requirement Management:</h4>

Las herramientas que vamos a especificar ahora, nos ayudaron a documentar, rastrear y verificar que cada requisito está implementado correctamente.

- **Git:** Es un sistema de control de versiones que se utiliza para rastrear los cambios en el código fuente durante el desarrollo de software. Permite a los desarrolladores trabajar en el mismo proyecto simultáneamente, facilitando la colaboración al permitirles crear, fusionar y gestionar diferentes versiones del código de manera eficiente. Funciona tomando instantáneas de los archivos cada vez que se confirma un cambio, almacenando un historial completo y seguro de todas las modificaciones. Lo usamos para registrar los cambios realizados del código dentro de github.

<h4>Product UX/UI Design: </h4>

Acá usamos una herramienta que nos permite diseñar pantallas, prototipos interactivos y flujos de navegación.

- **Figma:** Es una plataforma de diseño de interfaces que permite crear prototipos interactivos de forma colaborativa. Con esta herramienta diseñamos las pantallas de nuestro producto, tanto en su versión desktop como mobile, asegurando una experiencia de usuario clara, moderna y funcional. Además, nos permitió trabajar en equipo en tiempo real y compartir avances con facilidad.

<h4>Software Development:</h4>

Esta es la etapa donde vamos a especificar las herramientas que usamos para programar.

- **Visual Studio Code:** Es un editor de código fuente desarrollado por Microsoft que soporta múltiples lenguajes de programación. Lo empleamos para desarrollar el código del proyecto utilizando tecnologías como HTML y CSS.

- **GitHub:** Es una plataforma de alojamiento de repositorios basada en Git, que permite gestionar versiones del código y colaborar entre desarrolladores de manera organizada. La empleamos para almacenar nuestro proyecto en un repositorio remoto, realizar control de versiones y sincronizar los cambios realizados por cada integrante del equipo. Además, facilitó la revisión de código, la creación de ramas de desarrollo y la integración continua del producto.

<h4>Software Testing:</h4>

La herramienta que usamos para verificar que nuestro prototipo se vea correctamente.

- **Chrome:** Utilizamos el navegador Chrome para realizar las pruebas de visualización y comportamiento del prototipo, verificando su correcto funcionamiento en distintos tamaños de pantalla y su compatibilidad con los lenguajes de desarrollo implementados (HTML y CSS).

<h4>Software Documentation:</h4>

La herramienta especificada acá, nos permitió organizar, escribir y compartir la información del proyecto

- **.MD:** Un archivo con la extensión .md es un archivo de texto plano que utiliza el lenguaje de marcado Markdown, diseñado para ser legible y fácil de escribir. Usamos esta extensión para guardar documentación dentro del código.

### 5.1.2. Source Code Management. 

Para la gestión del código fuente del proyecto, el equipo utilizará Git como sistema de control de versiones distribuido, y GitHub como plataforma central de colaboración. Esto permitirá mantener un historial completo de los cambios realizados, facilitar el trabajo colaborativo entre los integrantes del equipo y asegurar la trazabilidad de todas las versiones del software.

<h4>Repositorios en Github</h4>

**Landing Page:** Repositorio público para la página de presentación del producto
https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page

**Acceptance Test:** Repositorio en el que se encuentran los archivos (.feature) en formato Gherkin.
https://github.com/1ASI0729-2620-4399-G3-Veygo/Veygo-AcceptanceTests

<h4>Implementación de Gitflow</h4>
El equipo adoptará el modelo de ramificación GitFlow, propuesto por Vincent Driessen, como flujo de trabajo estándar para el control de versiones.

<h4>Ramas principales</h4>

_main_: Contiene el código estable y listo para producción. Cada commit en esta rama representa una versión liberada del proyecto.
_develop_: Contiene el código con las últimas funcionalidades integradas, en preparación para la siguiente versión estable.  Es la base sobre la que se crean nuevas ramas de características (features).

<h4>Ramas de soporte</h4>
Además de las dos ramas principales, se implementarán las siguientes ramas temporales:

- Feature branches: Su propósito será desarrollar nuevas funcionalidades o mejoras.
- Release branches: Es para denominar una nueva versión estable del proyecto.
- Hotfix branches: Aca corregiremos errores críticos detectados en producción.

<h4>Semantic Versioning</h4>

_Aplicaremos Semantic Versioning 2.0.0_ para etiquetar las versiones del proyecto, con este formato:
**MAJOR.MINOR.PATCH**, siendo “MAJOR” un cambio incompatible con versiones anteriores, “MINOR” un agregado de nuevas funcionalidades y “PATCH” una corrección o mejoras sin afectar su compatibilidad.

- Ejemplo: v1.0.0 (primera versión), v1,1,0 (funcionalidad agregada) y v1.1.1 (corrección menor).

<h4>Conventional Commits</h4>

A partir de la segunda actualización (porque la primera llevará el nombre de “base”), los mensajes commit seguirán la especificación Conventional Commits, con el formato:  **tipo(especificación):descripción**
los tipos podrian ser: **feat** (nueva funcionalidad), **fix** (corrección de una parte del código), **docs**(cambios en la documentación), **style**(ajuste de formato), **refactor**(cambios en el codigo que no modifiquen la apariencia ni el comportamiento), **test** (modificación de prueba) y **chore** (tareas de mantenimiento o configuración)

- Ejemplo: feat(formulario): se agrego una validación al correo electrónico, fix(navbar): se corrigio error en la alineación, docs(README):se actualizo instrucciones.

<h4>Flujo general de trabajo</h4>

- Cada integrante clona el repositorio y crea su propia rama feature/ para trabajar en una nueva tarea.
- Cuando termina, se realiza un merge hacia develop mediante pull request.
Una vez integradas todas las funcionalidades planificadas, se crea una rama release/ para pruebas finales.
- Si la versión es aprobada, se fusiona a main, se etiqueta con su número de versión y se elimina la rama release/.
- En caso de detectar errores en producción, se genera una rama hotfix/ para resolverlos rápidamente.

### 5.1.3. Source Code Style Guide & Conventions. 

En esta sección se detallan las convenciones de estilo y las estructuras empleadas en el desarrollo del sitio web, abarcando los lenguajes HTML, CSS, JavaScript y Gherkin. Estas normas fueron adoptadas con el propósito de mantener un código limpio, organizado y fácilmente mantenible por todos los integrantes del equipo.

<h4> Convenciones HTML </h4>

- **Estructura semántica:** se utilizan etiquetas semánticas de HTML5 (`header`, `nav`, `main`, `section`, `article`, `footer`) en lugar de `div` genéricos, de modo que cada bloque de la página refleje su función dentro del documento.
- **Indentación:** 4 espacios por nivel de anidamiento, sin uso de tabulaciones.
- **Nomenclatura de atributos `id` y `class`:**
  - Los `id` se escriben en `camelCase` (`searchForm`, `formMessage`, `languageBtn`), ya que se utilizan como ganchos (*hooks*) para el JavaScript.
  - Las `class` se escriben en `kebab-case` (`segment-card`, `hero-copy`, `btn-primary`), siguiendo un patrón similar a BEM para variantes (`segment-card.owner` como modificador de `segment-card`).
- **Comentarios de sección:** cada bloque principal de la landing (`HERO`, `SEGMENTOS`, `CATEGORÍAS`, `TESTIMONIOS`, `CTA FINAL`, `FOOTER`) se delimita con un comentario HTML en mayúsculas, lo que facilita la navegación dentro del archivo:
```html
  <!-- HERO -->
  <section class="hero section" id="inicio">
    ...
  </section>
```
- **Espaciado entre bloques:** se deja una línea en blanco entre elementos hijos y dos líneas en blanco entre secciones distintas, priorizando la legibilidad sobre la compacidad del archivo.
- **Anclas de navegación:** los enlaces internos usan fragmentos (`#inicio`, `#buscar`, `#registro`) que coinciden exactamente con el `id` de la sección referenciada.
- **Internacionalización (i18n):** todo texto visible que deba traducirse incorpora un atributo `data-i18n` (o su variante) con una clave descriptiva en `snake_case`, que es resuelta en tiempo de ejecución por `script.js`:
  - `data-i18n` → contenido de texto plano.
  - `data-i18n-html` → contenido que admite HTML embebido (p. ej. saltos de línea o `span` con estilos).
  - `data-i18n-placeholder` → atributo `placeholder` de un `input`.
  - `data-i18n-aria` → atributo `aria-label`, para mantener la accesibilidad también traducida.
- **Accesibilidad:** toda etiqueta `img` incluye un atributo `alt` descriptivo; los controles interactivos que no tienen texto visible (como el botón de flecha `arrow-btn`) llevan `aria-label` mediante `data-i18n-aria`.

<h4> Convenciones CSS </h4>

- **Variables globales:** los colores, sombras y valores reutilizables se centralizan como propiedades personalizadas dentro de `:root`, con nombres en `kebab-case` prefijados con `--` (`--blue`, `--blue-dark`, `--muted`, `--shadow`). Esto evita valores "mágicos" repetidos y facilita el mantenimiento de la identidad visual de Veygo.
```css
  :root{
    --blue:#1464f4;
    --blue-dark:#0e1b45;
    --text:#17213d;
    --shadow:0 8px 28px rgba(22,39,76,.08);
  }
```
- **Reset base:** al inicio del archivo se normalizan márgenes, rellenos y `box-sizing` con un selector universal (`*{box-sizing:border-box;margin:0;padding:0}`), garantizando un comportamiento consistente entre navegadores.
- **Nomenclatura de clases:** `kebab-case` en todos los selectores (`.hero-copy`, `.segment-card`, `.final-cta-image`), evitando IDs para aplicar estilos (los `id` se reservan exclusivamente para JavaScript).
- **Estilo de escritura de reglas:** se combinan dos formatos según la complejidad del componente:
  - **Compacto en una sola línea** para reglas simples o utilitarias (`.brand{display:flex;align-items:center;gap:7px;...}`), priorizando la densidad del archivo.
  - **Expandido en múltiples líneas** para componentes con más propiedades o que requieren mayor claridad visual (`.process-item`, `.final-cta`), separando propiedades relacionadas con líneas en blanco.
- **Enfoque responsive:** el diseño es *desktop-first*; las adaptaciones a pantallas menores se definen con `@media (max-width: 900px)` y `@media (max-width: 600px)`, agrupando todas las reglas de un mismo breakpoint en un solo bloque al final de la hoja de estilos.
- **Medidas fluidas:** los anchos de sección se calculan con funciones modernas de CSS (`width:min(1400px,calc(100% - 80px))`) para adaptarse tanto a pantallas grandes como pequeñas sin necesidad de múltiples reglas fijas.
- **Comentarios:** se usan comentarios breves en mayúsculas para marcar subsecciones dentro de bloques largos (p. ej. `/* REDES */`, `/* PARTE INFERIOR */` dentro del `footer`).

<h4> Convenciones JavaScript </h4>

- **Organización por archivos:** la lógica de interacción se separa de los datos de traducción. `script.js` contiene únicamente comportamiento (eventos, validaciones, scroll), mientras que `language/es.js` y `language/en.js` exponen diccionarios de traducción como constantes globales (`translationsES`, `translationsEN`), cargados antes de `script.js` en el HTML.
- **Nomenclatura de variables y funciones:** `camelCase` para variables y funciones (`languageBtn`, `currentLanguage`, `cambiarIdioma`); las funciones con impacto directo en la interfaz se nombran en español, en línea con el resto del código orientado a negocio.
- **Diccionarios de traducción:** las claves de `translationsES` / `translationsEN` se agrupan por sección de la landing y se preceden de un comentario en mayúsculas (`// NAVBAR`, `// HERO`, `// SEGMENTOS`), replicando el mismo criterio de organización usado en el HTML y el CSS:
```javascript
  const translationsES = {

      // NAVBAR
      nav_home: "Inicio",
      nav_login: "Iniciar sesión",

      // HERO
      hero_badge: "✦ La nueva era de movilidad en Lima Metropolitana",
      hero_title: 'Encuentra el vehículo<br>que necesitas.',
  };
```
- **Selección de elementos del DOM:** se privilegia `document.getElementById` para elementos únicos referenciados por `id` (formularios, botones, contenedores) y `document.querySelectorAll` para colecciones de elementos que comparten una `class` o un atributo `data-*` (`.segment-card`, `[data-i18n]`).
- **Manejo de eventos:** los listeners se agregan con `addEventListener`, usando funciones flecha para callbacks cortos; cuando el evento no debe propagarse a manejadores externos (p. ej. el menú de idioma), se invoca explícitamente `event.stopPropagation()`.
- **Persistencia simple:** las preferencias del usuario que deben sobrevivir a un recargo de página (idioma seleccionado) se guardan en `localStorage` bajo una clave con prefijo del proyecto (`veygoLanguage`), evitando colisiones con otras claves genéricas.
- **Validaciones de formulario:** se realizan en el cliente antes de cualquier envío, mostrando el mensaje de error o éxito en un contenedor dedicado (`#formMessage`) en lugar de usar `alert()`, salvo en acciones de demostración explícitamente marcadas como tales.

<h4> Convenciones Gherkin </h4>

- **Organización de archivos:** cada historia de usuario se traduce en un archivo `.feature` independiente, nombrado con el patrón `USxx_titulo-de-la-historia.feature` (por ejemplo, `US15_publicacion_de_nuevo_vehiculo.feature`), lo que permite ubicar rápidamente el escenario correspondiente a cada historia.
- **Etiquetado (`tags`):** todo `Feature` incluye etiquetas `@USxx` y `@EP-xx` en la línea superior, para poder filtrar la ejecución de pruebas por historia individual o por épica completa (`cucumber --tags "@EP-07"`).
- **Estructura del encabezado:** cada `Feature` describe el objetivo de negocio siguiendo el formato "Como / quiero / para", manteniendo la trazabilidad directa con la historia de usuario original.
```gherkin
  @US17 @EP-07
  Feature: Solicitud de Reserva
    Como cliente
    quiero enviar una solicitud de alquiler
    para iniciar el proceso sin canales informales
```
- **Nomenclatura de escenarios:** los `Scenario` se nombran de forma breve y descriptiva en español, evitando ambigüedad (`Solicitud válida`, `Conflicto de fechas`).
- **Redacción de pasos:** cada paso `Given/When/Then` se redacta en tercera persona y en tiempo presente, distinguiendo dos niveles de lenguaje según el tipo de historia:
  - **Escenarios orientados a usuario final:** lenguaje de negocio, sin detalles técnicos (`Given vehículo disponible en las fechas seleccionadas`).
  - **Escenarios orientados a backend/API:** lenguaje técnico explícito, incluyendo verbo HTTP, ruta y código de respuesta esperado (`Given POST /bookings con fechas disponibles`, `Then el servidor retorna 201 con estado "pending"`).
- **Indentación:** 2 espacios para el encabezado del `Feature`, y 4 espacios para los `Scenario` y sus pasos `Given/When/Then`, manteniendo una jerarquía visual consistente en todo el archivo.
- **Separación de escenarios:** se deja una línea en blanco entre cada `Scenario` dentro de un mismo `Feature`, para facilitar la lectura cuando existen múltiples casos (éxito y error) por historia.

### 5.1.4. Software Deployment Configuration. 

En esta sección, daremos el paso a paso para realizar el deploy de nuestra página dentro de github.

<h4>Deploy con GitHub Pages: </h4>

Primero, nos ubicamos en el repositorio de GitHub de nuestro proyecto “landing-Page”  y nos dirigimos a los ajustes, ubicado en la parte superior en la barra horizontal.

![paso1](assets/img/Pas01.png)

Dentro de ajustes, nos dirigimos a la opción “Pages”  ubicada en la parte izquierda en un menú vertical.

![paso2](assets/img/Pas02.png)

Dentro, buscaras la sección “Branch”  donde encontraras un boton, el cual tiene por defecto “None”, entonces, seleccionamos el botón desplegable y eliges la opción “main”, posteriormente presionamos el botón “save”, para guardar los cambios y tenga efecto. 

![paso2](assets/img/Pas03.png)

Finalmente, tendrás que refrescar la página

![paso2](assets/img/Pas04.png)

Y con esto, podrás visualizar el link para visitar la página: https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/


## 5.2. Landing Page, Services & Applications Implementation. 

### 5.2.1. Sprint 1

Para este primer Sprint, el equipo estableció como objetivo principal la implementación y despliegue de la primera versión de la Landing Page del sistema Zyntra.

| ID   | User Story| Epic| Priority |SP |
| :-- | :-- | :-- | :-- | :-- |
| US08 | Navegación Principal y Selector de Idioma| EP-01 | High| 3  |
| US09 | Buscador Rápido de Vehículos| EP-01 | High| 3  |
| US10 | Exploración por Categorías de Propósito| EP-01 | Medium   | 2  |
| US11 | Visualización de Vehículos Destacados| EP-01 | Medium   | 3  |
| US12 | Redirección a Registro según Rol| EP-01 | Medium   | 2  |
| US22 | Sección de Confianza y Seguridad| EP-01 | Medium   | 2  |
| US23 | Sección de Preguntas Frecuentes| EP-01 | Low| 2  |
| US24 | Suscripción a Novedades| EP-01 | Low| 1  |
| US34 | Endpoint de Contenido Optimizado para Landing Page| EP-01 | Medium   | 3  |
| US35 | Endpoint de Recursos de Internacionalización (i18n)| EP-01 | High     | 3  |
| US36 | Endpoint de Registro de Eventos de Conversión| EP-01 | Medium   | 2  |
| | | |**Total Story Points**| **26** |

#### 5.2.1.1. Sprint Planning 1

| Campo | Detalle |
|---|---|
| **Sprint #** | Sprint 1 |
| **Fecha** | 2026-09-09 |
| **Hora** | 05:49 PM |
| **Lugar** | Reunión virtual vía Google Meet |
| **Preparado por** | Josue Antonio Flores Apaico|
| **Asistentes** |Josue Antonio Flores Apaico, Fabrizio Hamet Cano Ortiz, Marlon Alessandro Flores Siguas, Ivonne Beatriz Ibañez Torres y Eddo Su Caletti|
| **Resumen del Review del Sprint 0** | Durante la fase previa (Sprint 0), el equipo definió el backlog completo del producto (36 historias de usuario distribuidas en 9 épicas), redactó los criterios de aceptación en formato Gherkin para cada historia, y desarrolló una primera versión funcional de la landing page (HTML/CSS/JS) con selector de idioma ES/EN, buscador rápido y las secciones principales de valor. Sin embargo, esta versión aún no había sido validada formalmente contra los criterios de aceptación definidos ni conectada a los endpoints de backend planificados. |
| **Resumen de la Retrospectiva del Sprint 0** | El equipo identificó que, si bien se avanzó rápido en la construcción visual de la landing page, faltó verificar que cada sección cumpliera con los criterios de aceptación (Gherkin) de las historias de la épica EP-01, y que el contenido aún no estaba conectado a los endpoints de backend previstos (contenido cacheado, i18n, analítica de conversión). Se acordó que el Sprint 1 se enfocaría exclusivamente en cerrar esa brecha para la landing page antes de avanzar a otros módulos del sistema. |
| **Objetivo del Sprint 1** | Nuestro enfoque está en validar y perfeccionar la primera versión pública de la landing page de Veygo contra sus criterios de aceptación, y conectarla a sus dos endpoints de backend de soporte (contenido cacheado de landing e internacionalización) para que la experiencia sea completamente dinámica en lugar de estática. Consideramos que se entrega un producto listo para demo cuando un visitante puede abrir la landing page, cambiar instantáneamente entre español e inglés, realizar una búsqueda rápida de vehículos, explorar categorías y vehículos destacados, y ser redirigido al flujo de registro correcto (cliente o propietario) — todo esto validado contra los escenarios Gherkin de las historias US08 a US12, US22 a US24 y US34 a US36. Esto se confirmará mediante pruebas manuales end-to-end directamente sobre la URL desplegada de la landing page, verificadas contra los criterios de aceptación definidos en los archivos `.feature` correspondientes. |
| **Velocity del Sprint N** | 30 |
| **Suma de Story Points** | 27 |

#### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member | GitHub Username | Aspecto 1 (Estructura HTML — `index.html`) | Aspecto 2 (Estilos — `styles.css`) | Aspecto 3 (Interactividad — `script.js`) | Aspecto 4 (i18n Español — `es.js`) | Aspecto 5 (i18n Inglés — `en.js`) |
|---|---|---|---|---|---|---|
| **Flores Apaico, Josué Antonio** | **JosueFloresAp** | **L** | C | C | C | C |
| **Su Caletti, Eddo** | **Asalreon520** | C | **L** | C | C | C |
| **Ibañez Torres, Ivonne Beatriz** | **MarlonLasarte** | C | C | **L** | C | C |
| **Cano Ortiz, Fabrizio Hamet** | **Fabrizioco01**| C | C | C | **L** | C |
| **Flores Siguas, Marlon Alessandro** | **MarlonFS965** | C | C | C | C | **L** |

_(Nota: L = Leader, C = Collaborator)_

#### 5.2.1.3. Sprint Backlog 1

El objetivo principal de este Sprint fue implementar y desplegar la primera versión de la Landing Page del sistema Zyntra.

A continuación, se presenta una captura de pantalla del estado actual de nuestro tablero de control para el Sprint 1:

![sprint1](assets/img/sprin1.png)

Enlace del Jira: https://ivonneibanez.atlassian.net/jira/software/projects/PBV/boards/3?filter=&groupBy=none

| User Story ID | Título | Description (Task) | Estimation | Assigned To | Status |
|---|---|---|---|---|---|
| **US08** | Navegación Principal y Selector de Idioma | Implementación de la estructura en HTML (navbar y menú de idioma) | 2 hr | Josué | DONE |
| | | Implementación de diseño en CSS (navbar y dropdown de idioma) | 1 hr | Eddo | DONE |
| | | Implementación de la lógica del selector de idioma en JS | 2 hr | Ivonne | DONE |
| | | Implementación del diccionario de traducciones ES | 1 hr | Fabrizio | DONE |
| | | Implementación del diccionario de traducciones EN | 1 hr | Marlon | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Josué | DONE |
| **US09** | Buscador Rápido de Vehículos | Implementación de la estructura en HTML (formulario de búsqueda) | 2 hr | Josué | DONE |
| | | Implementación de diseño en CSS (search-box) | 1 hr | Eddo | DONE |
| | | Implementación de la validación del formulario en JS | 2 hr | Ivonne | DONE |
| | | Traducción de textos del buscador (ES) | 0.5 hr | Fabrizio | DONE |
| | | Traducción de textos del buscador (EN) | 0.5 hr | Marlon | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Eddo | DONE |
| **US10** | Exploración por Categorías de Propósito | Implementación de la estructura en HTML (category-grid) | 1 hr | Josué | DONE |
| | | Implementación de diseño en CSS (category-card) | 1 hr | Eddo | DONE |
| | | Traducción de categorías (ES) | 0.5 hr | Fabrizio | DONE |
| | | Traducción de categorías (EN) | 0.5 hr | Marlon | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Ivonne | DONE |
| **US11** | Visualización de Vehículos Destacados | Implementación de la estructura en HTML (vehicle-grid) | 2 hr | Josué | DONE |
| | | Implementación de diseño en CSS (vehicle-card) | 1 hr | Eddo | DONE |
| | | Traducción de textos de vehículos (ES) | 0.5 hr | Fabrizio | DONE |
| | | Traducción de textos de vehículos (EN) | 0.5 hr | Marlon | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Josué | DONE |
| **US12** | Redirección a Registro según Rol | Implementación de la estructura en HTML (segment-card) | 1 hr | Josué | DONE |
| | | Implementación de diseño en CSS (segment-card) | 1 hr | Eddo | DONE |
| | | Implementación de la lógica de redirección en JS | 1 hr | Ivonne | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Eddo | DONE |
| **US22** | Sección de Confianza y Seguridad | Implementación de la estructura en HTML (trust-grid) | 1 hr | Josué | DONE |
| | | Implementación de diseño en CSS (trust-grid) | 1 hr | Eddo | DONE |
| | | Traducción de textos de confianza (ES) | 0.5 hr | Fabrizio | DONE |
| | | Traducción de textos de confianza (EN) | 0.5 hr | Marlon | DONE |
| | | Revisión de funcionalidad y bugs | 1 hr | Ivonne | DONE |
| **US23** | Sección de Preguntas Frecuentes | Implementación de la estructura en HTML (acordeón de FAQ) | 2 hr | Josué | TO DO |
| | | Implementación de diseño en CSS (acordeón de FAQ) | 1 hr | Eddo | TO DO |
| | | Implementación de la lógica de apertura/cierre en JS | 1 hr | Ivonne | TO DO |
| | | Traducción de preguntas frecuentes (ES) | 1 hr | Fabrizio | TO DO |
| | | Traducción de preguntas frecuentes (EN) | 1 hr | Marlon | TO DO |
| **US24** | Suscripción a Novedades | Implementación de la estructura en HTML (formulario de suscripción) | 1 hr | Josué | TO DO |
| | | Implementación de diseño en CSS (formulario de suscripción) | 1 hr | Eddo | TO DO |
| | | Implementación de la validación de correo en JS | 1 hr | Ivonne | TO DO |
| | | Traducción de textos (ES) | 0.5 hr | Fabrizio | TO DO |
| | | Traducción de textos (EN) | 0.5 hr | Marlon | TO DO |

#### 5.2.1.4. Development Evidence for Sprint Review. 

El equipo trabajó de manera coordinada durante el desarrollo del proyecto, asignando tareas específicas a cada integrante de acuerdo con el flujo de trabajo establecido.

Posteriormente, cada miembro registró y subió sus avances al repositorio de GitHub, donde fueron revisados para su posterior integración en la rama `develop`.

Una vez finalizadas todas las tareas, el propietario del repositorio realizó la fusión de la rama `develop` con la rama `main`, permitiendo así habilitar la visualización de la landing page mediante GitHub Pages.

A continuación, se presentan los nombres de usuario de los integrantes del equipo, junto con algunos de los commits realizados por cada miembro:


| Repository | Branch | Commit Id | Commit Message | Commited by | Committed on (Date) |
|---|---|---|---|---|---|
|Landing-Page | main | 892b6456be9fbf25045372cc1dd3f12c3de51f19 | feat: add language | Josue Flores | 14/09/2026 |
|Landing-Page | main | 9b33ba0c6232d000fe2d1c756e20e8879847b953 | Script:GetElementByID |Ivonne Ibañez| 14/09/2026 |
|Landing-Page | main | f62792236b5f7651fc0c9132ae7f0b537848225a | ffeat(i18n): add Spanish testimonials and CTA translations | Marlon Flores | 14/09/2026 |
|Landing-Page | main | b0d22e7a162063e73c698e171a939e3932d460db | feat(i18n): add Spanish navbar and hero translations | Fabrizio Cano| 14/09/2026 |
|Landing-Page | main | b93de97144fe1ff04e0df6252eca680601b9b268 | feat: Last part of styles.css|Eddo Su| 14/09/2026 |

Enlace de historial de commits: https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page/commits/main/?before=892b6456be9fbf25045372cc1dd3f12c3de51f19+35

#### 5.2.1.5. Execution Evidence for Sprint Review

Al término del Sprint 1, el equipo logró implementar y desplegar satisfactoriamente la primera versión de la Landing Page del sistema Veygo. La página se encuentra disponible públicamente mediante GitHub Pages.

Link de la página: https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/

<h4>Navbar, Hero y estadísticas</h4>

![Veygo1](assets/img/Veygo1.png)

Barra de navegación con selector de idioma, hero principal ("Encuentra el vehículo que necesitas. Alquila con confianza.") con visual del vehículo, tarjetas de segmentación de usuarios (alquilar / publicar vehículo) y la banda de estadísticas de impacto (500+ vehículos, 1,200+ usuarios, 100% garantía, 4.9/5 satisfacción).

<h4>Buscador de vehículos y categorías</h4>

![Veygo2](assets/img/Veygo2.png)

Formulario "¿Dónde y cuándo necesitas un vehículo?" con campos de ubicación, fechas y necesidad, seguido de la sección de categorías con las 5 tarjetas filtrables (Trabajo diario, Familiar y viajes, Trabajo & carga, Aventura todo terreno, Premium & eléctricos), cada una con imagen representativa.

<h4>Proceso operativo y vehículos destacados</h4>

![Veygo3](assets/img/Veygo3.png)

Sección "Así funciona Veygo" con el flujo de 4 pasos (crear cuenta, encontrar vehículo, reservar y pagar, disfrutar el viaje), seguida del grid de vehículos destacados con imagen, tipo de transmisión, calificación, ubicación, capacidad de pasajeros y precio por día.

<h4>Confianza y testimonios</h4>

![Veygo4](assets/img/Veygo4.png)

Sección de Confianza con los tres pilares de seguridad (verificación de identidad con IA, registro de estado pre/post, calificaciones de reputación) y la sección de Testimonios con las tres reseñas de la comunidad (Renato, Mariana, Gianfranco), cada una con foto, rol y calificación de 5 estrellas.

<h4>CTA final y footer</h4>

Llamado a la acción de cierre ("¿Listo para vivir la movilidad del futuro en Lima?") con botones de registro gratuito y soporte por WhatsApp, junto con el footer completo: enlaces de navegación, soporte, redes sociales y datos de respaldo de Veygo S.A.C.

![Veygo5](assets/img/Veygo5.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1, el alcance de implementación se limitó exclusivamente al Landing Page estático. No se desarrollaron ni desplegaron Web Services (RESTful API) en esta iteración, por lo que no aplica documentación de endpoints para este Sprint. La documentación de servicios web se incorporará a partir del Sprint 2, conforme a lo planificado en el Product Backlog.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

Durante el Sprint 1, el alcance de la implementación y los objetivos definidos en el Sprint Backlog se centraron exclusivamente en el desarrollo de la Landing Page de Veygo. En esta etapa inicial, el equipo priorizó la creación de una interfaz principal que permitiera presentar de manera clara la propuesta de valor de la plataforma —conectar a propietarios y arrendatarios de vehículos en Lima Metropolitana de forma segura y transparente—, así como sus principales funcionalidades, a través de secciones como el Hero, la segmentación de usuarios, el buscador de vehículos, las categorías, el proceso operativo, los vehículos destacados, la Confianza y los Testimonios.

El trabajo realizado incluyó el diseño visual, la estructuración del contenido y la organización de las secciones clave de la Landing Page, asegurando una experiencia intuitiva, atractiva y alineada con las necesidades identificadas en las fases previas de investigación. Asimismo, se buscó que la página cumpliera con criterios básicos de usabilidad, coherencia visual y comunicación efectiva —reforzados con el soporte bilingüe español/inglés y el diseño responsive— facilitando que cualquier usuario comprenda rápidamente el propósito del sistema y los dos flujos principales del negocio: alquilar un vehículo o publicar el propio.

Cabe resaltar que, debido a la naturaleza introductoria de este Sprint, no se contempló el desarrollo de otras funcionalidades adicionales del sistema, como la conexión con el backend, el flujo completo de autenticación o el procesamiento real de reservas y pagos. El enfoque estuvo completamente orientado a establecer una base sólida a través de la Landing Page, la cual servirá como punto de partida para futuras iteraciones del proyecto. Las siguientes etapas del desarrollo, donde se abordarán nuevas funcionalidades y componentes del sistema —como la integración con el backend, el registro e inicio de sesión funcionales y la gestión real de vehículos y reservas—, se encuentran planificadas para los próximos Sprints, en los cuales se continuará ampliando progresivamente el alcance del producto.

#### 5.2.1.8. Team Collaboration Insights during Sprint

Durante este Sprint, el equipo concentró sus actividades de implementación y colaboración en el desarrollo de la Landing Page. Para garantizar un trabajo ordenado y con trazabilidad, se utilizó Git como sistema de control de versiones sobre un repositorio público alojado en GitHub, bajo la organización 1ASI0729-2620-4399-G3-Veygo.

A continuación, se presentan las capturas de los analíticos de GitHub que evidencian la participación, los commits y los additions de todos los miembros del equipo durante este Sprint:

![aditions general](assets/img/Commits_sprint1.png)

![commits](assets/img/additions_sprint1_users.png)

### 5.2.2. Sprint 2
Para el segundo Sprint, el equipo se enfocó en implementar y desplegar la primera versión del **Frontend Web Application** de Veygo. La aplicación permite a los arrendatarios buscar, reservar y calificar vehículos, y a los propietarios publicar su flota, gestionar la disponibilidad, atender solicitudes y revisar sus ingresos. La aplicación consume una Fake API (json-server) que simula los Web Services que se implementarán en el siguiente Sprint con ASP.NET Core.

| ID | User Story | Epic | Priority | SP |
| :-- | :-- | :-- | :-- | :-- |
| US02 | Inicio de Sesión Seguro | EP-02 | High | 3 |
| US03 | Búsqueda de Vehículos Cercanos | EP-03 | High | 5 |
| US04 | Filtrado por Transmisión y Energía | EP-04 | High | 3 |
| US15 | Publicación de Nuevo Vehículo | EP-05 | High | 5 |
| US16 | Edición o Retiro de Publicación | EP-05 | Medium | 3 |
| US05 | Sincronización Automática de Disponibilidad | EP-06 | High | 5 |
| US17 | Solicitud de Reserva | EP-07 | High | 5 |
| US18 | Confirmación o Rechazo de Solicitud | EP-07 | High | 3 |
| US19 | Cancelación de Reserva | EP-07 | Medium | 3 |
| US20 | Historial de Reservas | EP-07 | Medium | 2 |
| US21 | Notificaciones de Actividad | EP-07 | Medium | 3 |
| US06 | Métricas de Flota y Transacciones | EP-08 | Medium | 3 |
| US07 | Evaluación Mutua Post-Alquiler | EP-09 | Medium | 3 |
| US14 | Edición de Perfil de Usuario | EP-02 | Low | 2 |
| | | | **Total Story Points** | **48** |

#### 5.2.2.1.Sprint Planning 2.
La reunión de Sprint Planning 2 se realizó después de la revisión del Sprint 1. En ella el equipo revisó lo alcanzado con la Landing Page, acordó mejoras en la forma de trabajo y seleccionó las historias de usuario del Frontend Web Application que se implementarían en este Sprint.

| Campo | Detalle |
|---|---|
| **Sprint #** | Sprint 2 |
| **Fecha** | [YYYY-MM-DD] |
| **Hora** | [HH:MM PM] |
| **Lugar** | Reunión virtual vía Google Meet |
| **Preparado por** | Josue Antonio Flores Apaico |
| **Asistentes** | Josue Antonio Flores Apaico, Fabrizio Hamet Cano Ortiz, Marlon Alessandro Flores Siguas, Ivonne Beatriz Ibañez Torres y Eddo Su Caletti |
| **Resumen del Review del Sprint 1** | En el Sprint 1 se implementó y desplegó en GitHub Pages la primera versión de la Landing Page de Veygo, con navegación, selector de idioma (ES/EN), buscador rápido, categorías, vehículos destacados, sección de confianza y redirección al registro según el rol. Quedaron pendientes las secciones de preguntas frecuentes y suscripción a novedades. |
| **Resumen de la Retrospectiva del Sprint 1** | El equipo valoró la división del trabajo por archivos, pero identificó que los commits no siguieron siempre Conventional Commits y que se trabajó directamente sobre `main`. Para este Sprint se acordó aplicar GitFlow (ramas `feature/*` hacia `develop` mediante Pull Requests), usar Conventional Commits en inglés y organizar el código por bounded contexts. |
| **Objetivo del Sprint 2** | Nuestro enfoque está en entregar la primera versión del Frontend Web Application de Veygo, en la que el arrendatario puede buscar, reservar y calificar vehículos, y el propietario puede publicar su flota, gestionar su disponibilidad y atender las solicitudes. Creemos que esto entrega a arrendatarios y propietarios de Lima un canal confiable para alquilar vehículos sin intermediarios informales. Esto se confirmará cuando un arrendatario complete una reserva y el propietario la confirme desde la aplicación desplegada, viendo ambos la notificación correspondiente. |
| **Velocity del Sprint 2** | 50 |
| **Suma de Story Points** | 48 |

#### 5.2.2.2. Aspect Leaders and Collaborators.
Los aspectos de este Sprint corresponden a los bounded contexts del Frontend Web Application, definidos en el Design-Level EventStorming (sección 4.6.1), además de la configuración base y el despliegue. Cada integrante lideró al menos un aspecto y colaboró en la revisión de los Pull Requests de los demás.

| Team Member | GitHub Username | IAM, Shared, i18n y Router | Fleet | Booking | Engagement | Communication | Dashboard | Payment, Reputation y Notification | Deployment (Render y Firebase) |
|---|---|---|---|---|---|---|---|---|---|
| **Flores Apaico, Josué Antonio** | **JosueFloresAp** | **L** | **L** | C | C | C | C | **L** | **L** |
| **Su Caletti, Eddo** | **Asaltron520** | C | C | **L** | C | C | C | C | C |
| **Ibañez Torres, Ivonne Beatriz** | **MarlonLasarte** | C | C | C | C | C | **L** | C | C |
| **Cano Ortiz, Fabrizio Hamet** | **Fabrizioco01** | C | C | C | C | **L** | C | C | C |
| **Flores Siguas, Marlon Alessandro** | **MarlonFS965** | C | C | C | **L** | C | C | C | C |

_(Nota: L = Leader, C = Collaborator)_


#### 5.2.2.3. Sprint Backlog 2

El objetivo principal de este Sprint fue implementar y desplegar la primera versión del Frontend Web Application de Veygo, organizada por bounded contexts y conectada a una Fake API desplegada.

A continuación, se presenta una captura de pantalla del tablero de control para el Sprint 2:

![sprint2](assets/img/sprint2/sprint2-board.png)

Enlace del Jira: https://ivonneibanez.atlassian.net/jira/software/projects/PBV/boards/3?filter=&groupBy=none

| Sprint # | Sprint 2 | | | | | | |
|---|---|---|---|---|---|---|---|
| **Story Id** | **Story Title** | **Task Id** | **Task Title** | **Task Description** | **Estimation (Hours)** | **Assigned To** | **Status** |
| US02 | Inicio de Sesión Seguro | T01 | Modelo de dominio IAM | Implementar la entidad `User`, `UserRole`, `DriverLicense` y `UserPreferences`. | 2 | Josué | Done |
| | | T02 | Servicio y store de IAM | Implementar `IamApi`, `UserAssembler`, almacenamiento de sesión y el store de IAM. | 3 | Josué | Done |
| | | T03 | Vistas de inicio de sesión y registro | Implementar las vistas de sign-in y sign-up por rol, con validaciones. | 3 | Josué | Done |
| | | T04 | Guardas de navegación | Proteger las rutas privadas y separar las vistas por rol. | 2 | Josué | Done |
| US14 | Edición de Perfil de Usuario | T05 | Vista de perfil | Implementar la edición de datos personales, foto, licencia, preferencias y contraseña. | 3 | Josué | Done |
| US03 | Búsqueda de Vehículos Cercanos | T06 | Modelo y API de Fleet | Implementar `Vehicle`, `VehicleLocation`, `FleetApi` y `VehicleAssembler`. | 3 | Josué | Done |
| | | T07 | Búsqueda con mapa | Implementar la vista de búsqueda con mapa de OpenStreetMap (Leaflet) y tarjetas de vehículos. | 4 | Josué | Done |
| US04 | Filtrado por Transmisión y Energía | T08 | Filtros de catálogo | Implementar `VehicleSearchCriteria` (Specification) y el panel de filtros. | 3 | Josué | Done |
| US15 | Publicación de Nuevo Vehículo | T09 | Formulario de vehículo | Implementar el formulario con carga de fotos, especificaciones y tarifas. | 4 | Josué | Done |
| US16 | Edición o Retiro de Publicación | T10 | Gestión de flota | Implementar Mis vehículos, el detalle del propietario, edición y publicar/retirar. | 3 | Josué | Done |
| US05 | Sincronización Automática de Disponibilidad | T11 | Calendario de disponibilidad | Implementar el calendario con días reservados y el bloqueo y desbloqueo de fechas. | 4 | Josué | Done |
| US17 | Solicitud de Reserva | T12 | Modelo y store de Booking | Implementar la entidad `Booking`, el assembler, la API y el store con validación de disponibilidad. | 4 | Eddo | Done |
| | | T13 | Confirmación de reserva | Implementar la vista de confirmación con el cálculo del total. | 3 | Eddo | Done |
| US18 | Confirmación o Rechazo de Solicitud | T14 | Solicitudes del propietario | Implementar la vista de reservas del propietario con aceptar y rechazar. | 2 | Eddo | Done |
| US19 | Cancelación de Reserva | T15 | Cancelación | Implementar la cancelación desde las reservas del arrendatario y del propietario. | 1 | Eddo | Done |
| US20 | Historial de Reservas | T16 | Mis reservas | Implementar la lista de reservas del arrendatario con filtro por estado. | 2 | Eddo | Done |
| US21 | Notificaciones de Actividad | T17 | Contexto Notification | Implementar la entidad, la API, el store y los handlers de eventos de dominio. | 3 | Josué | Done |
| | | T18 | Campana de notificaciones | Implementar el componente de notificaciones en la barra superior. | 2 | Josué | Done |
| | | T19 | Mensajería | Implementar conversaciones y mensajes entre arrendatario y propietario. | 4 | Fabrizio | Done |
| US06 | Métricas de Flota y Transacciones | T20 | Panel del propietario | Implementar el inicio del propietario con métricas y accesos rápidos. | 3 | Ivonne | Done |
| | | T21 | Transacciones | Implementar el historial de transacciones, el gráfico por vehículo y el reporte CSV. | 3 | Josué | Done |
| US07 | Evaluación Mutua Post-Alquiler | T22 | Reseñas | Implementar el registro de reseñas y la vista de calificaciones con nivel de reputación. | 3 | Josué | Done |
| — | Favoritos (soporte de US03) | T23 | Vehículos favoritos | Implementar el contexto Engagement y la vista de favoritos. | 2 | Marlon | Done |
| — | Inicio del arrendatario | T24 | Panel del arrendatario | Implementar el inicio del arrendatario con búsqueda rápida y recomendados. | 2 | Ivonne | Done |
| — | Configuración base | T25 | Shared kernel e i18n | Implementar `BaseApi`, `BaseEndpoint`, error interceptor, value objects, layout e idiomas EN/ES. | 4 | Josué | Done |
| — | Fake API | T26 | Fake API | Implementar la base de datos y rutas de json-server con datos de prueba. | 2 | Josué | Done |
| — | Despliegue | T27 | Despliegue | Desplegar la Fake API en Render y la aplicación en Firebase Hosting. | 2 | Josué | Done |

#### 5.2.2.4. Development Evidence for Sprint Review

Durante este Sprint se implementó la primera versión del Frontend Web Application de Veygo con Vue 3, JavaScript, PrimeVue, Vue Router, Pinia, vue-i18n, Axios y Leaflet. El código se organizó por bounded contexts (IAM, Fleet, Booking, Engagement, Reputation, Payment, Communication, Notification y Dashboard), cada uno con sus capas domain, infrastructure, application y presentation.

El equipo aplicó GitFlow: cada funcionalidad se desarrolló en su propia rama `feature/*`, que se integró a `develop` mediante Pull Requests (#1 al #14). Finalmente, `develop` se integró a `main` (Pull Request #15) para el despliegue. Todos los mensajes siguen Conventional Commits.

Repositorio del Frontend Web Application: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| 1ASI0729-2620-4399-G3-Veygo/frontend | main | f68ef1f | chore: initial commit | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | d8e5c0c | feat(fleet): add vehicle entity, value objects and search criteria | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | 1a2c9aa | feat(fleet): add fleet api and vehicle assembler | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | daf735e | feat(fleet): add fleet and availability stores | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | 25a5ea3 | feat(fleet): add vehicle card, filters, map and calendar components | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | e58e8a0 | feat(fleet): add vehicle search, detail, form and availability views | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | 199b954 | build: add project dependencies | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | f5bf814 | chore: remove example store | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | 18f32cb | feat(iam): add user entity, user role, driver license and preferences | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | a0c6715 | feat(iam): add iam api, user assembler and session storage | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | bf7e240 | feat(iam): add iam store | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | 8af593e | feat(iam): add auth panel, auth scene, role option and user profile components | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | 6dfdd4b | feat(iam): add sign-in, sign-up and profile views | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | ab370f8 | build: add leaflet and json-server dependencies | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/i18n | 37aac26 | chore(i18n): add vue-i18n configuration | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/notification | 20a50b1 | feat(notification): add notification entity | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/payment | 85e8f1b | feat(payment): add transaction entity and income summary | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | e624b06 | feat(reputation): add review entity and reputation summary | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | 1258c73 | feat(reputation): add reputation api, resources and review assembler | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | 14cc09d | feat(reputation): add reputation store | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | bbf4f6c | feat(reputation): add review item and review dialog components | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | 1a5b01e | feat(reputation): add owner ratings view | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/router | 63df29b | feat(router): add routes and role-based navigation guard | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | c163b09 | feat(shared): add value objects money, date range, date time, url and string validator | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 2e4202c | feat(shared): add domain event bus | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 218489a | feat(api): add base api and base endpoint | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | f762ef5 | feat(api): add error interceptor | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | cb34cc2 | feat(shared): add image file reader | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 055127a | feat(shared): add formatting composable, lima districts and theme helper | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 6e618e4 | feat(ui): add layout, top bar, navigation menu, footer and language switcher | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 2335354 | feat(ui): add page header, stat card, bar chart and unavailable content components | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 9462bcc | feat(ui): add page not found and terms and conditions views | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 6ebf174 | feat(booking): implement booking store with availability validation and status lifecycle actions. | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | b989b62 | feat(booking): implement booking store with availability validation and status lifecycle actions. | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 39f3f1f | feat(booking): implement booking store with availability validation and status lifecycle actions. | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 907a74f | feat(creation):Create Booking | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 546a5e3 | Delete src/Booking | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | ca75a6a | Create booking.store.js | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | d844441 | Delete src/application directory | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 7a8bd60 | Create booking.entity.js | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | e3a3638 | Delete src/booking/domain/model directory | — | Eddo Su caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | af146c0 | implement booking store with availability validation and status lifecycle actions | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 6fa347d | add Booking domain entity with validation, pricing, and lifecycle methods | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | d896e2b | implement data mapper assembler and API service client for bookings | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 8e66b5c | implement BookingItem, BookingStatusFilter, and BookingStatusTag UI components | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | b9e4f31 | add useBookingDetails composable to resolve vehicle and user references | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 04cbdc0 | implement booking confirmation view, owner requests dashboard, and renter bookings list | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | b9e1f2f | refactor name booking-api | — | Asaltron520 | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 43690c7 | feat(engagement): add favorite vehicles view | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | c8aad59 | feat(engagement): add favorite entity | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 1b227ce | feat(engagement): add favorite assembler | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 9c9ecfb | feat(engagement): add engagement resources | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 0cca9c9 | feat(engagement): add engagement api | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 035c433 | feat(engagement): add engagement store | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | cd3d35b | feat(communication): add communication store | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 2bfc308 | feat(communication): add conversation entity | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 235ae82 | fix(communication): correct communication store path | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 228c06f | fix(communication): remove incorrect communication store path | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | ad9bcd1 | feat(communication): add message entity | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | b136891 | feat(communication): add communication api | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | fce1560 | feat(communication): add communication resources | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 8c2363a | feat(communication): add conversation assembler | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 941d108 | feat(communication): add message assembler | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | cf2d1e8 | feat(communication): add messages view | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/dashboard | 1c75905 | FEATURE(dashboard):quick-actions | — | MarlonLasarte | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/dashboard | 3b23a82 | FEATURE(dashboard):owner-home | — | MarlonLasarte | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/dashboard | 10473d4 | FEATURE(dashboard):renter-home | — | MarlonLasarte | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 2a36108 | chore: add environment files | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 652d172 | chore: add favicon, brand, vehicle and avatar images | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 455e824 | style: add veygo global styles and design tokens | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 8049332 | feat(app): register primevue, i18n, pinia and router and restore session | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | b7b0e93 | feat(fake-api): add json-server database and routes | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | ffdd01d | build: add fake-api script | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 9972fed | fix(build): move fake-api script into scripts section | — | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | main | db4889c | feat(firebase): add firebase hosting configuration | — | Josue Flores | 05/10/2026 |

_(Los commits no incluyen un cuerpo de mensaje; la descripción completa del cambio está en el título del commit.)_

Enlace del historial de commits: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/commits/main

Enlace de los Pull Requests: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/pulls?q=is%3Apr+is%3Aclosed

#### 5.2.2.5. Execution Evidence for Sprint Review

Al término del Sprint 2, el equipo implementó y desplegó la primera versión del Frontend Web Application de Veygo. La aplicación ofrece dos experiencias según el rol del usuario: el arrendatario puede buscar vehículos por ubicación, fechas y tipo, revisar su detalle, reservarlos, guardarlos como favoritos, calificar sus alquileres y conversar con el propietario; el propietario puede publicar y editar vehículos, gestionar su disponibilidad, aceptar o rechazar solicitudes, revisar sus transacciones y calificaciones, y recibir notificaciones. La interfaz está disponible en inglés (idioma por defecto) y en español, y se adapta a pantallas móviles.

Link de la aplicación: https://veygo-web-app.web.app

Link del video: [URL del video en Microsoft Stream]

Cuentas de prueba (contraseña `Veygo2026!`): `leo.ramos@veygo.pe` (arrendatario) y `laura.torres@veygo.pe` (propietario).

<h4>Inicio de sesión y registro</h4>

![Inicio de sesión](assets/img/sprint2/exec-01-sign-in.png)

Vista de inicio de sesión con el formulario sobre una escena animada de carretera nocturna y selector de idioma.

![Registro](assets/img/sprint2/exec-02-sign-up.png)

Registro con selección de rol (arrendatario o propietario). Los campos cambian según el rol elegido y el mensaje de la derecha se adapta al tipo de usuario.

<h4>Arrendatario: inicio y búsqueda</h4>

![Inicio del arrendatario](assets/img/sprint2/exec-03-renter-home.png)

Inicio del arrendatario con buscador por ubicación, fecha de inicio, fecha fin y tipo de vehículo, accesos por categoría, vehículos recomendados, mapa de vehículos cercanos y próximas reservas.

![Búsqueda de vehículos](assets/img/sprint2/exec-04-vehicle-search.png)

Búsqueda con filtros por precio, transmisión, combustible y calificación, resultados disponibles en las fechas elegidas y mapa de OpenStreetMap con el precio de cada vehículo.

<h4>Arrendatario: detalle y reserva</h4>

![Detalle del vehículo](assets/img/sprint2/exec-05-vehicle-detail.png)

Detalle del vehículo con galería, especificaciones, ubicación de recojo, datos del propietario y selección de fechas.

![Confirmación de reserva](assets/img/sprint2/exec-06-booking-confirmation.png)

Confirmación de la reserva con el resumen de días, precio y depósito. Antes de crearla, el sistema verifica que las fechas no se crucen con otra reserva o con días bloqueados.

![Mis reservas](assets/img/sprint2/exec-07-renter-bookings.png)

Historial de reservas filtrable por estado, con opciones para cancelar y calificar los alquileres finalizados.

![Favoritos](assets/img/sprint2/exec-08-favorites.png)

Vehículos guardados como favoritos.

<h4>Comunicación, notificaciones y perfil</h4>

![Mensajes](assets/img/sprint2/exec-09-messages.png)

Mensajería entre arrendatario y propietario.

![Notificaciones](assets/img/sprint2/exec-10-notifications.png)

Campana de notificaciones con los cambios de estado de las reservas y los mensajes nuevos.

![Perfil](assets/img/sprint2/exec-11-profile.png)

Perfil del usuario con datos personales, licencia de conducir, estadísticas y preferencias de idioma, notificaciones y modo oscuro.

<h4>Propietario: inicio y flota</h4>

![Inicio del propietario](assets/img/sprint2/exec-12-owner-home.png)

Inicio del propietario con métricas de vehículos, próximas reservas, ingresos del mes y calificación promedio, junto con accesos rápidos.

![Mis vehículos](assets/img/sprint2/exec-13-owner-vehicles.png)

Gestión de la flota: búsqueda, filtros, publicación o retiro, edición y detalle de cada vehículo.

![Detalle del vehículo para el propietario](assets/img/sprint2/exec-14-owner-vehicle-detail.png)

Detalle del vehículo desde la perspectiva del propietario, con precios, información adicional, disponibilidad y estadísticas.

![Agregar vehículo](assets/img/sprint2/exec-15-vehicle-form.png)

Formulario de publicación con datos básicos, especificaciones, equipamiento, información adicional y carga de fotos.

<h4>Propietario: disponibilidad, reservas, transacciones y calificaciones</h4>

![Disponibilidad](assets/img/sprint2/exec-16-availability.png)

Calendario de disponibilidad por vehículo con días reservados, pendientes y bloqueados, y acciones para bloquear o desbloquear fechas.

![Reservas del propietario](assets/img/sprint2/exec-17-owner-bookings.png)

Solicitudes de reserva con opciones para aceptar o rechazar, y filtros por estado y vehículo.

![Transacciones](assets/img/sprint2/exec-18-transactions.png)

Transacciones con rango de fechas editable, resumen de ingresos, gráfico por mes y por vehículo, historial y descarga del reporte.

![Calificaciones](assets/img/sprint2/exec-19-ratings.png)

Calificaciones con el promedio, la distribución de estrellas, las reseñas de los clientes y la calificación por vehículo.

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

En este Sprint no se implementaron los Web Services en ASP.NET Core; están planificados para el siguiente Sprint, donde se documentarán con OpenAPI (Swagger). Para que el Frontend Web Application funcione con datos reales, el equipo implementó una **Fake API** con json-server, que expone los mismos recursos REST que tendrá la API definitiva bajo el prefijo `/api/v1`. La Fake API está desplegada en Render.

URL base: https://veygo-fake-api.onrender.com/api/v1

Repositorio (carpeta `server/`): https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/tree/main/server

| Recurso | Endpoint | Acciones utilizadas | Sintaxis de llamada | Parámetros | Uso en la aplicación |
|---|---|---|---|---|---|
| Users | `/users` | GET, PATCH, DELETE | `GET /api/v1/users?email={email}` <br> `GET /api/v1/users/{id}` <br> `PATCH /api/v1/users/{id}` | `email`, `password`, `id` | Inicio de sesión, registro, perfil y eliminación de cuenta. |
| Users | `/users` | POST | `POST /api/v1/users` | Body: datos del usuario | Registro de arrendatarios y propietarios. |
| Vehicles | `/vehicles` | GET, POST, PUT, PATCH, DELETE | `GET /api/v1/vehicles?published=true` <br> `GET /api/v1/vehicles?ownerId={id}` <br> `GET /api/v1/vehicles/{id}` | `published`, `ownerId`, `id` | Catálogo, búsqueda, detalle y gestión de la flota. |
| Bookings | `/bookings` | GET, POST, PATCH | `GET /api/v1/bookings?renterId={id}` <br> `GET /api/v1/bookings?ownerId={id}` <br> `GET /api/v1/bookings?vehicleId={id}` <br> `PATCH /api/v1/bookings/{id}` | `renterId`, `ownerId`, `vehicleId` | Solicitud, confirmación, rechazo, cancelación e historial de reservas. |
| Blocked dates | `/blockedDates` | GET, POST, DELETE | `GET /api/v1/blockedDates?vehicleId={id}` | `vehicleId` | Bloqueo y desbloqueo de fechas en el calendario. |
| Favorites | `/favorites` | GET, POST, DELETE | `GET /api/v1/favorites?renterId={id}` | `renterId` | Vehículos favoritos. |
| Reviews | `/reviews` | GET, POST | `GET /api/v1/reviews?vehicleId={id}` <br> `GET /api/v1/reviews?ownerId={id}` | `vehicleId`, `ownerId` | Reseñas y reputación. |
| Conversations | `/conversations` | GET, POST, PATCH | `GET /api/v1/conversations?ownerId={id}` <br> `GET /api/v1/conversations?renterId={id}` | `ownerId`, `renterId` | Lista de conversaciones. |
| Messages | `/messages` | GET, POST | `GET /api/v1/messages?conversationId={id}` | `conversationId` | Mensajes de una conversación. |
| Notifications | `/notifications` | GET, POST, PATCH | `GET /api/v1/notifications?userId={id}` | `userId` | Campana de notificaciones. |

Ejemplo de respuesta de `GET /api/v1/bookings/1`:

```json
{
  "id": 1,
  "vehicleId": 1,
  "renterId": 1,
  "ownerId": 2,
  "startDate": "2026-10-05",
  "endDate": "2026-10-08",
  "pricePerDay": 180,
  "totalPrice": 540,
  "status": "confirmed",
  "paymentMethod": "card",
  "createdAt": "2026-09-20T14:10:00Z",
  "confirmedAt": "2026-09-21T09:00:00Z"
}
```

La respuesta devuelve la reserva con el vehículo, el arrendatario y el propietario relacionados, el periodo de alquiler, el precio y el estado (`pending`, `confirmed`, `rejected`, `cancelled` o `completed`).

Ejemplo de respuesta de `GET /api/v1/reviews?vehicleId=1` (primer elemento):

```json
{
  "id": 1,
  "bookingId": 7,
  "vehicleId": 1,
  "ownerId": 2,
  "renterId": 5,
  "rating": 5,
  "comment": "The car was spotless and very comfortable. Laura was attentive and communication was excellent. Totally recommended!",
  "createdAt": "2026-04-13T18:00:00Z"
}
```

![Fake API desplegada](assets/img/sprint2/fake-api-vehicles.png)

Respuesta de `GET /api/v1/vehicles` desde la Fake API desplegada en Render.

| Repository | Branch | Commit Id | Commit Message | Committed by | Committed on (Date) |
|---|---|---|---|---|---|
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | b7b0e93 | feat(fake-api): add json-server database and routes | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | ffdd01d | build: add fake-api script | Josue Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 9972fed | fix(build): move fake-api script into scripts section | Josue Flores | 05/10/2026 |

#### 5.2.2.7. Software Deployment Evidence for Sprint Review

En este Sprint se desplegaron dos productos: la **Fake API** en Render y el **Frontend Web Application** en Firebase Hosting. Ambos se despliegan desde la rama `main` del repositorio `frontend`.

| Producto | Plataforma | URL |
|---|---|---|
| Landing Page | GitHub Pages | https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/ |
| Frontend Web Application | Firebase Hosting | https://veygo-web-app.web.app |
| Fake API (json-server) | Render | https://veygo-fake-api.onrender.com/api/v1 |

<h4>Despliegue de la Fake API en Render</h4>

1. Se creó una cuenta en Render y se eligió la opción **New → Web Service**.

![Render nuevo servicio](assets/img/sprint2/deploy-01-render-new-service.png)

2. Se seleccionó **Public Git Repository** y se indicó el repositorio `frontend` de la organización.

![Render repositorio público](assets/img/sprint2/deploy-02-render-public-repo.png)

3. Se configuró el servicio con el nombre `veygo-fake-api`, el entorno **Node**, la rama `main` y el directorio raíz `server`, donde se encuentra la Fake API.

![Render configuración](assets/img/sprint2/deploy-03-render-settings.png)

4. Se definieron el comando de inicio `npm start` y la instancia gratuita. En el primer intento el comando de build incluía `npm run build`, que no existe en la Fake API, por lo que se corrigió a `npm install` desde *Settings*.

![Render comandos e instancia](assets/img/sprint2/deploy-04-render-commands-free.png)

5. El despliegue terminó correctamente y el servicio quedó disponible en `https://veygo-fake-api.onrender.com`.

![Render desplegado](assets/img/sprint2/deploy-05-render-live.png)

<h4>Despliegue del Frontend Web Application en Firebase Hosting</h4>

1. Se creó el proyecto `veygo-web-app` en la consola de Firebase, en el plan gratuito Spark.

![Firebase crear proyecto](assets/img/sprint2/deploy-06-firebase-create-project.png)

![Firebase proyecto creado](assets/img/sprint2/deploy-07-firebase-project.png)

2. Se instaló Firebase CLI con `npm install -g firebase-tools`.

![Firebase CLI](assets/img/sprint2/deploy-08-firebase-cli-install.png)

3. Se inició sesión con `firebase login` y se vinculó el proyecto con `firebase use --add`, lo que generó el archivo `.firebaserc`. Además se creó `firebase.json`, que publica la carpeta `dist` y redirige todas las rutas a `index.html` para que funcione el enrutamiento de la SPA.

![Firebase login](assets/img/sprint2/deploy-09-firebase-login.png)

4. Se generó la versión de producción con `npm run build`. Esta versión usa `.env.production`, que apunta a la Fake API desplegada en Render.

![Build de producción](assets/img/sprint2/deploy-10-npm-build.png)

5. Se desplegó con `firebase deploy --only hosting`. La aplicación quedó disponible en `https://veygo-web-app.web.app`.

![Firebase deploy](assets/img/sprint2/deploy-11-firebase-deploy.png)

La configuración de Firebase se registró en el repositorio con el commit `db4889c feat(firebase): add firebase hosting configuration`.

#### 5.2.2.8. Team Collaboration Insights during Sprint

Durante este Sprint el equipo trabajó en el repositorio `frontend` de la organización 1ASI0729-2620-4399-G3-Veygo aplicando GitFlow. Cada integrante desarrolló su bounded context en una rama `feature/*` y la integró a `develop` mediante Pull Requests; luego `develop` se integró a `main` para el despliegue.

| Integrante | Rama(s) | Commits |
|---|---|---|
| Flores Apaico, Josué Antonio | feature/fleet, feature/iam, feature/i18n, feature/notification, feature/payment, feature/reputation, feature/router, feature/shared, feature/app-setup | 40 |
| Su Caletti, Eddo | feature/booking | 16 |
| Cano Ortiz, Fabrizio Hamet | feature/communication | 10 |
| Flores Siguas, Marlon Alessandro | feature/engagement | 6 |
| Ibañez Torres, Ivonne Beatriz | feature/dashboard | 3 |

A continuación, se presentan las capturas de los analíticos de GitHub que evidencian la participación de los miembros del equipo durante este Sprint:

![Contributors](assets/img/sprint2/insights-contributors.png)

![Commits](assets/img/sprint2/insights-commits.png)

![Network](assets/img/sprint2/insights-network.png)
