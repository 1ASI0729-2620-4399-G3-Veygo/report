# Capítulo V: Product Implementation, Validation & Deployment.

## 5.1. Software Configuration Management.

Software Configuration Management (SCM), es un conjunto de actividades y procesos que tiene como objetivo organizar y supervisar los cambios que se realizan en el software durante su desarrollo, usaremos esto para garantizar que nuestro producto se mantenga consistente, funcional y confiable, a medida que evoluciona con el tiempo. 

### 5.1.1. Software Development Environment Configuration.

En esta sección se presentan los productos de software que el equipo utilizó para colaborar en el desarrollo de Veygo, organizados según las actividades del ciclo de vida del proyecto: Project Management, Requirement Management, Product UX/UI Design, Software Development, Software Testing, Software Deployment y Software Documentation.

<h4>Project Management</h4>

Herramientas utilizadas para planificar los Sprints, dar seguimiento a las tareas y mantener la comunicación del equipo.

- **Jira Software:** herramienta de gestión ágil en la que el equipo administró el Product Backlog, las Epics, las User Stories y las Technical Stories, y organizó cada Sprint en un tablero con los estados To Do, In Process, To Review y Done. Disponible en: https://ivonneibanez.atlassian.net/jira/software/projects/PBV/boards/3
- **WhatsApp:** aplicación de mensajería que el equipo utilizó como canal principal de coordinación, mediante un grupo privado en el que se compartieron avances, archivos y enlaces, y se acordaron las fechas límite de cada entrega.
- **Discord:** plataforma de comunicación por voz y texto que se utilizó para las reuniones de Sprint Planning, Sprint Review y Retrospective, así como para resolver dudas en tiempo real durante el desarrollo.

<h4>Requirement Management</h4>

Herramientas utilizadas para documentar, priorizar y verificar los requisitos del producto.

- **Jira Software:** se utilizó para registrar las User Stories y Technical Stories con su Epic, su estimación en Story Points y su prioridad, de modo que cada ítem del Product Backlog mantiene el mismo identificador que en el informe.
- **Gherkin:** lenguaje con el que se redactaron los criterios de aceptación de cada historia en archivos `.feature`, siguiendo la estructura Given–When–Then. Estos archivos se encuentran en el repositorio de Acceptance Tests: https://github.com/1ASI0729-2620-4399-G3-Veygo/Veygo-AcceptanceTests

<h4>Product UX/UI Design</h4>

Herramientas utilizadas para la investigación de usuarios, el diseño de la experiencia y el modelado del dominio.

- **Figma:** herramienta de diseño colaborativo con la que se elaboraron la guía de estilos, los wireframes, los mock-ups y el prototipo de la Landing Page y del Frontend Web Application.
- **UXPressia:** plataforma en la que se elaboraron los User Personas, los User Journey Maps, los Empathy Maps y el Impact Mapping.
- **Miro:** pizarra colaborativa que se utilizó para el Big Picture EventStorming, el Design-Level EventStorming, los User Flow Diagrams y el flujo del prototipo.
- **Structurizr:** herramienta de Diagram-as-Code con la que se elaboraron los diagramas del C4 Model (Context, Container y Component).
- **Mermaid:** lenguaje de Diagram-as-Code con el que se elaboraron los Class Diagrams y los Database Diagrams.

<h4>Software Development</h4>

Herramientas, lenguajes y librerías utilizados para programar los productos de software.

- **WebStorm y Visual Studio Code:** entornos de desarrollo con los que se programaron la Landing Page y el Frontend Web Application.
- **HTML5, CSS3 y JavaScript:** tecnologías con las que se desarrolló la Landing Page, incluyendo el soporte de idiomas español e inglés.
- **Vue 3 (v3.5) y Vite (v8):** framework de JavaScript y herramienta de construcción con los que se desarrolló el Frontend Web Application como una Single-Page Application organizada por bounded contexts.
- **PrimeVue (v5) y PrimeIcons:** librería de componentes de interfaz utilizada para construir las vistas de la aplicación con un diseño consistente.
- **Vue Reactivity API (`reactive`):** se utilizó para implementar los stores de la capa de aplicación de cada bounded context (por ejemplo, `bookingStore` o `fleetStore`), que mantienen el estado y coordinan las llamadas a la API.
- **Vue Router (v5):** librería de enrutamiento con la que se definieron las rutas de la aplicación y las guardas de navegación por rol (arrendatario y propietario).
- **vue-i18n (v11):** librería de internacionalización que permite mostrar la aplicación en inglés y en español.
- **Axios (v1):** cliente HTTP con el que la capa de infraestructura consume los endpoints de la Fake API.
- **Leaflet y OpenStreetMap:** librería y servicio de mapas con los que se implementó la búsqueda de vehículos cercanos.
- **json-server (v0.17):** herramienta con la que se implementó la Fake API que simula los Web Services de Veygo durante el Sprint 2.
- **Git y GitHub:** sistema de control de versiones y plataforma de repositorios con los que el equipo aplicó GitFlow, trabajó en ramas `feature/*` e integró los cambios mediante Pull Requests. Los repositorios del proyecto se detallan en la sección 5.1.2.

<h4>Software Testing</h4>

Herramientas utilizadas para verificar el funcionamiento y la adaptabilidad de los productos.

- **Google Chrome y Chrome DevTools:** navegador y herramientas de desarrollo con los que se verificó el comportamiento de la Landing Page y del Frontend Web Application, se inspeccionaron las peticiones a la Fake API y se probó el diseño responsive en distintos tamaños de pantalla.
- **Gherkin:** los escenarios de los archivos `.feature` se utilizaron como guía para validar manualmente que cada funcionalidad implementada cumpliera sus criterios de aceptación.

<h4>Software Deployment</h4>

Plataformas utilizadas para publicar los productos de software y hacerlos accesibles desde Internet.

- **GitHub Pages:** servicio con el que se desplegó la Landing Page desde la rama `main` de su repositorio: https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/
- **Firebase Hosting:** servicio con el que se desplegó el Frontend Web Application mediante Firebase CLI: https://veygo-web-app.web.app
- **Render:** plataforma en la que se desplegó la Fake API como Web Service de Node.js: https://veygo-fake-api.onrender.com/api/v1

<h4>Software Documentation</h4>

Herramientas utilizadas para elaborar la documentación del proyecto y del código.

- **Markdown y GitHub:** el informe del proyecto se redactó en archivos Markdown en el repositorio `report`, de forma colaborativa mediante ramas y Pull Requests.
- **JSDoc:** convención de comentarios con la que se documentaron las clases, entidades, servicios y stores del Frontend Web Application.

### 5.1.2. Source Code Management.

Para la gestión del código fuente, el equipo utilizó Git como sistema de control de versiones distribuido y GitHub como plataforma de colaboración. Todos los repositorios del proyecto se encuentran en la organización **1ASI0729-2620-4399-G3-Veygo**, lo que permite mantener un historial completo de los cambios, trabajar de forma paralela y asegurar la trazabilidad entre el código, las User Stories y los Sprints.

<h4>Repositorios en GitHub</h4>

| Producto | Repositorio | Descripción |
|:---|:---|:---|
| Organización | https://github.com/1ASI0729-2620-4399-G3-Veygo | Agrupa todos los repositorios del proyecto. |
| Informe del proyecto | https://github.com/1ASI0729-2620-4399-G3-Veygo/report | Documentación del Trabajo Final en formato Markdown. |
| Landing Page | https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page | Sitio estático de presentación del producto (HTML, CSS y JavaScript). |
| Frontend Web Application | https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend | Single-Page Application desarrollada con Vue 3, que incluye la Fake API en la carpeta `server/`. |
| Acceptance Tests | https://github.com/1ASI0729-2620-4399-G3-Veygo/Veygo-AcceptanceTests | Archivos `.feature` en Gherkin con los criterios de aceptación de las User Stories y Technical Stories. |
| RESTful API (Backend) | https://github.com/1ASI0729-2620-4399-G3-Veygo/backend | Repositorio creado para los Web Services en ASP.NET Core, cuya implementación inicia en el Sprint 3. |

<h4>Workflow de ramificación: GitFlow</h4>

El equipo adoptó el modelo de ramificación GitFlow, propuesto por Vincent Driessen, como flujo de trabajo para el control de versiones.

**Ramas principales**

- `main`: contiene el código estable y listo para producción. Es la rama desde la que se despliega cada producto.
- `develop`: integra las funcionalidades terminadas antes de pasarlas a `main`. Es la base desde la que se crean las ramas de funcionalidad.

**Ramas de soporte**

- `feature/*`: se crea una rama por funcionalidad o bounded context a partir de `develop`, por ejemplo `feature/fleet`, `feature/booking` o `feature/communication`. Al terminar, se integra a `develop` mediante un Pull Request.
- `release/*`: se crea desde `develop` para preparar una nueva versión estable antes de integrarla a `main`.
- `hotfix/*`: se crea desde `main` para corregir errores críticos detectados en producción, y se integra tanto a `main` como a `develop`.

**Aplicación en cada repositorio**

| Repositorio | Ramas utilizadas | Aplicación de GitFlow |
|:---|:---|:---|
| `frontend` | `main`, `develop`, `feature/app-setup`, `feature/shared`, `feature/router`, `feature/i18n`, `feature/iam`, `feature/fleet`, `feature/booking`, `feature/engagement`, `feature/communication`, `feature/dashboard`, `feature/payment`, `feature/reputation`, `feature/notification` | Cada integrante desarrolló su bounded context en una rama `feature/*`, que se integró a `develop` mediante los Pull Requests #1 al #14. Luego `develop` se integró a `main` con el Pull Request #15 para el despliegue. |
| `report` | `main`, `develop`, `Capitulo1` a `Capitulo5`, `StudentOutcome` | Cada capítulo se elaboró en su propia rama, que se integró a `develop` y luego a `main` mediante Pull Requests. |
| `landing-Page` | `main` | En el Sprint 1 se trabajó directamente sobre `main`. En la retrospectiva del Sprint 1 se identificó esta práctica como una oportunidad de mejora, y a partir del Sprint 2 se aplicó GitFlow completo. |
| `Veygo-AcceptanceTests` | `main` | Repositorio de documentación con una sola rama, ya que sus archivos no se despliegan. |

**Flujo general de trabajo**

1. El integrante actualiza `develop` y crea su rama `feature/<nombre>`.
2. Realiza sus commits siguiendo Conventional Commits.
3. Publica la rama y abre un Pull Request hacia `develop`, que es revisado por otro integrante del equipo.
4. Cuando las funcionalidades del Sprint están integradas, `develop` se integra a `main` mediante un Pull Request y se despliega.
5. La versión publicada se etiqueta en `main` siguiendo Semantic Versioning.

<h4>Semantic Versioning</h4>

Las versiones de los productos se identifican con Semantic Versioning 2.0.0, con el formato **MAJOR.MINOR.PATCH**:

- **MAJOR:** cambios incompatibles con versiones anteriores.
- **MINOR:** nuevas funcionalidades compatibles con la versión anterior.
- **PATCH:** correcciones que no afectan la compatibilidad.

Ejemplo: `v1.0.0` (primera versión estable), `v1.1.0` (nueva funcionalidad) y `v1.1.1` (corrección menor).

| Repositorio | Versión | Contenido |
|:---|:---|:---|
| `landing-Page` | `v1.0.0` | Primera versión de la Landing Page (Sprint 1). |
| `landing-Page` | `v1.1.0` | Redirección de los CTA y del buscador al Frontend Web Application (Sprint 2). |
| `frontend` | `v1.0.0` | Primera versión del Frontend Web Application integrada con la Fake API (Sprint 2). |

<h4>Conventional Commits</h4>

Los mensajes de commit siguen la especificación Conventional Commits, redactados en inglés y con el formato:

```
<type>(<scope>): <description>
```

Los tipos utilizados son:

| Tipo | Uso |
|:---|:---|
| `feat` | Nueva funcionalidad. |
| `fix` | Corrección de un error. |
| `docs` | Cambios en la documentación. |
| `style` | Cambios de formato o estilos que no alteran la lógica. |
| `refactor` | Reestructuración del código sin cambiar su comportamiento. |
| `test` | Creación o modificación de pruebas. |
| `build` | Cambios en dependencias o en la configuración de construcción. |
| `chore` | Tareas de mantenimiento o configuración. |

El `scope` indica el bounded context o el módulo afectado. Ejemplos tomados de los repositorios del proyecto:

- `feat(fleet): add vehicle entity, value objects and search criteria`
- `fix(communication): correct communication store path`
- `build: add fake-api script`
- `style: add veygo global styles and design tokens`
- `docs(chapter3): add user stories US37-US50 and technical stories TS51-TS57 with acceptance scenarios`

### 5.1.3. Source Code Style Guide & Conventions.

En esta sección se detallan las convenciones de estilo y de nomenclatura que el equipo aplicó en los productos de Veygo: la Landing Page (HTML, CSS y JavaScript), el Frontend Web Application (Vue 3 y JavaScript) y los Acceptance Tests (Gherkin). Estas convenciones permiten mantener un código limpio, organizado y fácil de mantener por todos los integrantes del equipo. Como regla general, los nombres en el código, los comentarios técnicos y los mensajes de commit se escriben en inglés, de acuerdo con el Ubiquitous Language definido en la sección 2.5.

Como referencia se tomaron las siguientes guías:

- Google HTML/CSS Style Guide: https://google.github.io/styleguide/htmlcssguide.html
- Vue.js Style Guide: https://vuejs.org/style-guide/
- Gherkin Reference: https://cucumber.io/docs/gherkin/reference/
- Conventional Commits: https://www.conventionalcommits.org/en/v1.0.0/

<h4>Landing Page: convenciones HTML</h4>

- **Estructura semántica:** se utilizan etiquetas semánticas de HTML5 (`header`, `nav`, `main`, `section`, `article`, `footer`) en lugar de `div` genéricos, de modo que cada bloque refleje su función dentro del documento.
- **Indentación:** 4 espacios por nivel de anidamiento, sin tabulaciones.
- **Atributos `id` y `class`:**
  - Los `id` se escriben en `camelCase` (`searchForm`, `formMessage`, `languageBtn`) y se reservan como ganchos (*hooks*) para JavaScript.
  - Las `class` se escriben en `kebab-case` (`segment-card`, `hero-copy`, `btn-primary`), con un patrón similar a BEM para las variantes (`segment-card owner`).
- **Comentarios de sección:** cada bloque principal se delimita con un comentario HTML en mayúsculas (`<!-- HERO -->`, `<!-- FOOTER -->`).
- **Anclas de navegación:** los enlaces internos usan fragmentos (`#inicio`, `#buscar`) que coinciden con el `id` de la sección.
- **Internacionalización:** todo texto visible incorpora un atributo con una clave en `snake_case`, que `script.js` resuelve en tiempo de ejecución: `data-i18n` (texto), `data-i18n-html` (texto con HTML), `data-i18n-placeholder` (placeholder) y `data-i18n-aria` (`aria-label`).
- **Accesibilidad:** toda imagen incluye un atributo `alt` descriptivo, y los controles sin texto visible llevan `aria-label`.

```html
<!-- HERO -->
<section class="hero section" id="inicio">
    <h1 data-i18n-html="hero_title">Encuentra el vehículo<br>que necesitas.</h1>
</section>
```

<h4>Landing Page: convenciones CSS</h4>

- **Variables globales:** los colores, sombras y valores reutilizables se declaran como propiedades personalizadas en `:root`, en `kebab-case` (`--blue`, `--blue-dark`, `--text`, `--shadow`), y se reutilizan con `var()` en toda la hoja de estilos.
- **Reset base:** al inicio del archivo se normalizan márgenes, rellenos y `box-sizing` con un selector universal.
- **Nomenclatura de clases:** `kebab-case` en todos los selectores. No se utilizan `id` para aplicar estilos.
- **Formato de las reglas:** las reglas simples se escriben en una sola línea y las de los componentes con más propiedades, en varias líneas.
- **Diseño responsive:** se aplica un enfoque *desktop-first*, con las adaptaciones agrupadas al final del archivo en `@media (max-width: 900px)` y `@media (max-width: 600px)`.
- **Medidas fluidas:** los anchos de sección se calculan con funciones de CSS como `width: min(1400px, calc(100% - 80px))`.

```css
:root {
    --blue: #2563EB;
    --blue-dark: #172554;
    --shadow: 0 8px 28px rgba(22, 39, 76, .08);
}
```

<h4>Landing Page: convenciones JavaScript</h4>

- **Organización por archivos:** `script.js` contiene solo el comportamiento (eventos, validaciones y scroll), mientras que `language/es.js` y `language/en.js` contienen los diccionarios de traducción (`translationsES`, `translationsEN`), agrupados por sección.
- **Nomenclatura:** `camelCase` para variables y funciones (`languageBtn`, `currentLanguage`) y `UPPER_SNAKE_CASE` para constantes globales.
- **Selección del DOM:** `document.getElementById` para elementos únicos y `document.querySelectorAll` para colecciones (`[data-i18n]`).
- **Eventos:** los listeners se registran con `addEventListener` y funciones flecha para callbacks cortos.
- **Persistencia:** el idioma seleccionado se guarda en `localStorage` con una clave que lleva el prefijo del proyecto (`veygoLanguage`).
- **Validaciones:** los formularios se validan antes de enviarse, y los mensajes se muestran en un contenedor dedicado (`#formMessage`) en lugar de `alert()`.

<h4>Frontend Web Application: organización del código</h4>

El código fuente se organiza por **bounded context**, siguiendo los contextos definidos en el Design-Level EventStorming (sección 4.6.1). Cada contexto se divide en cuatro capas:

```
src/
├── booking/                    # Un directorio por bounded context
│   ├── domain/model/           # Entidades, value objects y enumeraciones
│   ├── application/            # Store del contexto (estado y casos de uso)
│   ├── infrastructure/         # API, resources y assemblers
│   └── presentation/           # Vistas, componentes y composables
│       ├── views/
│       ├── components/
│       └── composables/
├── fleet/  iam/  engagement/  communication/  payment/
├── reputation/  notification/  dashboard/
├── shared/                     # Shared kernel: BaseApi, value objects, layout
├── router/index.js             # Rutas y guardas de navegación
├── locales/en.json, es.json    # Textos de la interfaz
├── i18n.js
└── main.js
```

- **Dependencias entre capas:** `presentation` usa `application` y `domain`; `application` usa `infrastructure` y `domain`; `domain` no depende de ninguna otra capa. Los value objects compartidos (`Money`, `DateRange`, `DateTime`) y los componentes de layout se ubican en `shared`.
- **Imports:** se utiliza el alias `@/` para referenciar la carpeta `src` (`@/shared/domain/model/money.js`), e incluyen siempre la extensión del archivo.

<h4>Frontend Web Application: nomenclatura</h4>

| Elemento | Convención | Ejemplo |
|:---|:---|:---|
| Carpetas | `kebab-case`, en singular para los bounded contexts | `booking/`, `presentation/components/` |
| Entidades | `<nombre>.entity.js` | `booking.entity.js` |
| Value objects y enumeraciones | `<nombre>.js` | `date-range.js`, `booking-status.js` |
| Stores | `<contexto>.store.js` | `booking.store.js` |
| Servicios de API | `<contexto>-api.js` | `booking-api.js` |
| Resources | `<contexto>-resources.js` | `booking-resources.js` |
| Assemblers | `<nombre>.assembler.js` | `booking.assembler.js` |
| Vistas | `kebab-case.vue`, nombradas por pantalla | `owner-bookings.vue`, `booking-confirmation.vue` |
| Componentes | `kebab-case.vue`, nombrados por elemento | `booking-item.vue`, `booking-status-tag.vue` |
| Composables | `use-<nombre>.js`, que exporta `use<Nombre>` | `use-booking-details.js` → `useBookingDetails` |
| Clases | `PascalCase` | `Booking`, `BookingApi`, `BookingAssembler` |
| Instancias de store | `camelCase` con sufijo `Store` | `bookingStore`, `fleetStore` |
| Variables y funciones | `camelCase` | `loadRenterBookings`, `formatMoney` |
| Enumeraciones | `PascalCase` con valores en minúsculas | `BookingStatus.CONFIRMED = 'confirmed'` |
| Rutas | `kebab-case`, con prefijo de rol | `/renter/bookings`, `/owner/vehicles` |
| Claves de i18n | `kebab-case`, agrupadas por contexto | `booking.cancel-booking` |
| Variables de entorno | `UPPER_SNAKE_CASE` con prefijo `VITE_` | `VITE_VEYGO_API_URL` |

<h4>Frontend Web Application: estilo de código</h4>

- **Componentes:** todos los componentes y vistas utilizan `<script setup>` (Composition API), con el orden `<script setup>`, `<template>` y `<style scoped>`.
- **Uso de componentes:** los componentes se importan en `PascalCase` y se usan con esa misma notación en el template (`<PageHeader />`, `<VehicleSpecs />`).
- **Formato:** 4 espacios de indentación, comillas simples en JavaScript y punto y coma al final de cada instrucción.
- **Stores:** cada store es un objeto reactivo (`reactive`) que expone el estado (`loading`, `errors` y los datos del contexto) y acciones que devuelven una `Promise`. Las vistas no llaman a la API directamente: lo hacen a través del store.
- **Infraestructura:** cada servicio de API extiende `BaseApi` y define sus endpoints con `BaseEndpoint`. Los assemblers convierten las respuestas de la API en entidades del dominio y viceversa.
- **Textos:** ningún texto visible se escribe directamente en el template; todos se obtienen de `locales/en.json` y `locales/es.json` mediante `t('<contexto>.<clave>')`.
- **Documentación:** las clases, los stores y sus métodos se documentan con JSDoc (`@param`, `@returns`, `@type`).

```javascript
/**
 * Application service (store) for the Booking bounded context.
 */
export const bookingStore = reactive({
    /** @type {Booking[]} Bookings of the signed-in renter. */
    renterBookings: [],
    loading: false,
    errors: [],

    /**
     * Loads the bookings of a renter.
     * @param {number} renterId - The renter identifier.
     * @returns {Promise<void>}
     */
    loadRenterBookings(renterId) {
        this.loading = true;
        return bookingApi.getBookingsByRenterId(renterId)
            .then(response => {
                this.renterBookings = BookingAssembler.toEntitiesFromResponse(response);
            });
    }
});
```

<h4>Acceptance Tests: convenciones Gherkin</h4>

- **Organización de archivos:** cada historia se traduce en un archivo `.feature` independiente, nombrado con su identificador y su título en `snake_case`: `USxx_titulo_de_la_historia.feature` para las User Stories y `TSxx_titulo_de_la_historia.feature` para las Technical Stories (por ejemplo, `US17_solicitud_de_reserva.feature`).
- **Etiquetas:** cada `Feature` incluye las etiquetas de la historia y de su Epic (`@US17 @EP-07`), para filtrar la ejecución por historia o por Epic.
- **Encabezado:** cada `Feature` describe la historia con el formato "Como / quiero / para", lo que mantiene la trazabilidad con la sección 3.1.
- **Escenarios:** los `Scenario` se nombran de forma breve y descriptiva en español, e incluyen el flujo principal y al menos un flujo alternativo.
- **Redacción de pasos:** los pasos se escriben en tercera persona y en tiempo presente. En las User Stories se usa lenguaje de negocio, y en las Technical Stories se indica el verbo HTTP, la ruta y el código de respuesta esperado.
- **Formato:** 2 espacios de indentación para el `Feature`, 4 para los `Scenario` y sus pasos, y una línea en blanco entre escenarios.

```gherkin
@US17 @EP-07
Feature: Solicitud de reserva
  Como cliente
  quiero enviar una solicitud de alquiler
  para iniciar el proceso sin canales informales

    Scenario: Fechas disponibles
      Given el cliente tiene su identidad verificada
      When solicita un vehículo para un rango de fechas disponible
      Then el sistema registra la reserva en estado "Pendiente"
```


### 5.1.4. Software Deployment Configuration.

En esta sección se describe la configuración utilizada para desplegar los productos de Veygo y hacerlos accesibles desde Internet. Cada producto se despliega desde la rama `main` de su repositorio, de modo que solo el código integrado y revisado mediante Pull Requests llega a producción.

| Producto | Plataforma | Repositorio y origen | Build | URL |
|:---|:---|:---|:---|:---|
| Landing Page | GitHub Pages | `landing-Page`, rama `main`, carpeta raíz | No requiere (sitio estático) | https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/ |
| Frontend Web Application | Firebase Hosting | `frontend`, rama `main`, carpeta `dist` | `npm run build` | https://veygo-web-app.web.app |
| Fake API | Render (Web Service, Node.js) | `frontend`, rama `main`, carpeta `server` | `npm install` | https://veygo-fake-api.onrender.com/api/v1 |

<h4>Variables de entorno del Frontend Web Application</h4>

El Frontend Web Application obtiene la URL de la API desde variables de entorno de Vite, por lo que el mismo código funciona en desarrollo y en producción sin modificaciones:

| Archivo | Uso | `VITE_VEYGO_API_URL` |
|:---|:---|:---|
| `.env.development` | `npm run dev` (entorno local) | `http://localhost:3000/api/v1` |
| `.env.production` | `npm run build` (despliegue) | `https://veygo-fake-api.onrender.com/api/v1` |

Las claves privadas, como la licencia de PrimeUI, se definen en `.env.local`, archivo que no se sube al repositorio.

<h4>Despliegue de la Landing Page en GitHub Pages</h4>

1. En el repositorio `landing-Page`, se ingresó a **Settings**, ubicado en la barra superior.

![Paso 1: Settings del repositorio](assets/img/Pas01.png)

2. En el menú lateral izquierdo, se seleccionó la opción **Pages**.

![Paso 2: Opción Pages](assets/img/Pas02.png)

3. En la sección **Build and deployment**, se eligió **Deploy from a branch** como origen, y en **Branch** se seleccionó la rama `main` con la carpeta raíz (`/root`). Luego se presionó **Save**.

![Paso 3: Selección de la rama main](assets/img/Pas03.png)

4. Después de unos minutos, al actualizar la página, GitHub Pages muestra la URL pública del sitio. Cada nuevo commit en `main` vuelve a publicar la Landing Page de forma automática.

![Paso 4: Sitio publicado](assets/img/Pas04.png)

<h4>Despliegue del Frontend Web Application en Firebase Hosting</h4>

El Frontend Web Application se despliega como sitio estático en Firebase Hosting (plan gratuito Spark), en el proyecto `veygo-web-app`. La configuración se registra en el archivo `firebase.json` del repositorio:

```json
{
  "hosting": {
    "public": "dist",
    "ignore": ["firebase.json", "**/.*", "**/node_modules/**"],
    "rewrites": [{ "source": "**", "destination": "/index.html" }]
  }
}
```

- `public: "dist"` indica que se publica la carpeta generada por `npm run build`.
- La regla `rewrites` redirige todas las rutas a `index.html`, lo que permite que Vue Router resuelva rutas como `/renter/bookings` al recargar la página.

El proceso de despliegue sigue estos comandos:

```bash
npm install -g firebase-tools   # Instala Firebase CLI (una sola vez)
firebase login                  # Inicia sesión con la cuenta del proyecto
firebase use --add              # Vincula el proyecto veygo-web-app (.firebaserc)
npm run build                   # Genera la carpeta dist con .env.production
firebase deploy --only hosting  # Publica la aplicación
```

<h4>Despliegue de la Fake API en Render</h4>

La Fake API se despliega en Render como un **Web Service** de Node.js, a partir de la carpeta `server` del repositorio `frontend`. Su archivo `server/package.json` define el comando de inicio:

```json
{
  "scripts": {
    "start": "json-server db.json --routes routes.json --host 0.0.0.0 --port ${PORT:-3000}"
  },
  "dependencies": {
    "json-server": "0.17.4"
  }
}
```

La configuración del servicio en Render es la siguiente:

| Parámetro | Valor |
|:---|:---|
| Nombre del servicio | `veygo-fake-api` |
| Lenguaje | Node |
| Rama | `main` |
| Root Directory | `server` |
| Build Command | `npm install` |
| Start Command | `npm start` |
| Tipo de instancia | Free |

El archivo `routes.json` agrega el prefijo `/api/v1` a todos los recursos, de modo que la Fake API expone las mismas rutas que tendrá la RESTful API. Render vuelve a desplegar el servicio de forma automática con cada commit en `main`.

En el plan gratuito, el servicio se suspende tras un periodo de inactividad, por lo que la primera petición puede tardar hasta un minuto en responder.

Las capturas del proceso completo de despliegue en Render y en Firebase Hosting se presentan en la sección 5.2.2.7.

## 5.2. Landing Page, Services & Applications Implementation. 

### 5.2.1. Sprint 1

Para el primer Sprint, el equipo estableció como objetivo implementar y desplegar la primera versión de la Landing Page de **Veygo**. La Landing Page presenta la propuesta de valor del producto, permite cambiar el idioma entre español e inglés, iniciar una búsqueda rápida de vehículos y dirigir al visitante al registro según su rol (cliente o propietario).

El alcance del Sprint comprende las User Stories de la Epic EP-01 (Landing Page y Captura de Interés) que corresponden al sitio estático. Las Technical Stories TS34, TS35 y TS36, que exponen endpoints de soporte para la Landing Page, se planificaron para los Sprints en los que se implementa la RESTful API.

| ID | User Story | Epic | Priority | Story Points |
| :-- | :-- | :-- | :-- | :--: |
| US08 | Navegación principal y selector de idioma | EP-01 | High | 3 |
| US09 | Buscador rápido de vehículos | EP-01 | High | 3 |
| US10 | Exploración por categorías de propósito | EP-01 | Medium | 2 |
| US11 | Visualización de vehículos destacados | EP-01 | Medium | 2 |
| US12 | Redirección a registro según rol | EP-01 | High | 2 |
| US22 | Sección de confianza y seguridad | EP-01 | Medium | 1 |
| US48 | Sección "Cómo funciona" | EP-01 | Medium | 1 |
| US49 | Sección de testimonios | EP-01 | Low | 1 |
| US23 | Sección de preguntas frecuentes | EP-01 | Low | 1 |
| US24 | Suscripción a novedades | EP-01 | Low | 2 |
| | | | **Total Story Points** | **18** |

#### 5.2.1.1. Sprint Planning 1

La reunión de Sprint Planning 1 se realizó al inicio de la implementación del producto, después de completar los artefactos de investigación, especificación y diseño de los Capítulos I al IV. En ella, el equipo definió el objetivo del Sprint, seleccionó las User Stories de la Landing Page desde el Product Backlog y distribuyó las tareas entre los integrantes.

| Campo | Detalle |
|---|---|
| **Sprint #** | Sprint 1 |
| **Fecha** | 2026-09-09 |
| **Hora** | 05:49 PM |
| **Lugar** | Reunión virtual vía Google Meet |
| **Preparado por** | Josue Antonio Flores Apaico |
| **Asistentes** | Josue Antonio Flores Apaico, Fabrizio Hamet Cano Ortiz, Marlon Alessandro Flores Siguas, Ivonne Beatriz Ibañez Torres y Eddo Su Caletti |
| **Resumen del Review del Sprint anterior** | No aplica, ya que es el primer Sprint de implementación. Como punto de partida, el equipo contaba con el Product Backlog priorizado, los criterios de aceptación en Gherkin, la guía de estilos, la arquitectura de información y los wireframes y mock-ups de la Landing Page elaborados en el Capítulo IV. |
| **Resumen de la Retrospectiva del Sprint anterior** | No aplica, ya que es el primer Sprint de implementación. Para este Sprint, el equipo acordó dividir el trabajo por archivo de la Landing Page (estructura HTML, estilos CSS, interactividad en JavaScript y diccionarios de traducción) para que cada integrante pudiera avanzar en paralelo. |
| **Objetivo del Sprint 1** | Nuestro enfoque está en publicar la primera versión de la Landing Page de Veygo, que presenta la propuesta de valor del producto en español e inglés. Creemos que esto permite a los visitantes de Lima entender cómo funciona Veygo, confiar en la plataforma y decidir si registrarse como cliente o como propietario. Esto se confirmará cuando un visitante pueda abrir la Landing Page desplegada en GitHub Pages, cambiar el idioma, realizar una búsqueda rápida, explorar las categorías y los vehículos destacados, y llegar al registro según su rol, de acuerdo con los criterios de aceptación de las User Stories del Sprint. |
| **Velocity del Sprint 1** | 20 |
| **Suma de Story Points** | 18 |

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

Durante este Sprint se implementó la primera versión de la Landing Page de Veygo con HTML5, CSS3 y JavaScript. El trabajo se distribuyó por archivo, de acuerdo con los aspectos definidos en la sección 5.2.1.2:

- **Estructura HTML (`index.html`):** Josue Flores implementó las secciones de la página (navbar, hero, segmentos, estadísticas, buscador, categorías, proceso, vehículos destacados, confianza, testimonios, CTA final y footer).
- **Estilos (`styles.css`):** Eddo Su Caletti implementó el diseño visual y las reglas responsive.
- **Interactividad (`script.js`):** Ivonne Ibañez implementó el selector de idioma, la validación del buscador y los eventos de la página.
- **Traducción al español (`language/es.js`):** Fabrizio Cano implementó el diccionario de textos en español.
- **Traducción al inglés (`language/en.js`):** Marlon Flores implementó el diccionario de textos en inglés.

En este Sprint, los integrantes registraron sus avances directamente en la rama `main` del repositorio `landing-Page`, desde la que se publica el sitio en GitHub Pages. En la retrospectiva del Sprint se identificó que esta práctica, junto con algunos mensajes de commit que no siguieron Conventional Commits, debía mejorarse. Por ello, a partir del Sprint 2 el equipo aplicó GitFlow con ramas `feature/*`, Pull Requests hacia `develop` y commits en inglés con el formato Conventional Commits.

Repositorio de la Landing Page: https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page

A continuación, se presentan los commits más representativos de cada integrante. El historial completo del Sprint 1 está compuesto por 46 commits.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 23c1076 | feat: add index.html | — | Josue Flores | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 0ca627e | feat: add search | — | Josue Flores | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 892b645 | feat: add language | — | Josue Flores | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | a8bd74c | feat: first part of styles.css | — | Eddo Su Caletti | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 1a2666c | feat: Part four of styles.css | — | Eddo Su Caletti | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | b93de97 | feat: Last part of styles.css | — | Eddo Su Caletti | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 9b33ba0 | Script:GetElementByID | — | Ivonne Ibañez | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 9cadf40 | Script:Cambio de idioma | — | Ivonne Ibañez | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 8ff16bb | Script:Event | — | Ivonne Ibañez | 15/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | b0d22e7 | feat(i18n): add Spanish navbar and hero translations | — | Fabrizio Cano | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 97e3ee2 | feat(i18n): add Spanish search and category translations | — | Fabrizio Cano | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | f1bdf85 | feat(i18n): add Spanish footer and form messages | — | Fabrizio Cano | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | b501a56 | feat: add English navbar and hero translations | — | Marlon Flores | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | 69e7396 | feat: add English vehicle and trust translations | — | Marlon Flores | 14/09/2026 |
| 1ASI0729-2620-4399-G3-Veygo/landing-Page | main | f376d85 | feat: add English footer and form messages | — | Marlon Flores | 14/09/2026 |

Enlace del historial de commits: https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page/commits/main

#### 5.2.1.5. Execution Evidence for Sprint Review

Al término del Sprint 1, el equipo logró implementar y desplegar satisfactoriamente la primera versión de la Landing Page del sistema Veygo. La página se encuentra disponible públicamente mediante GitHub Pages.

Link de la página: https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/

Link del video de la Landing: https://drive.google.com/file/d/1l8ePdIv1fKThjkbrtdvrguK2p1-xVeVd/view?usp=sharing

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

En este Sprint se desplegó la primera versión de la Landing Page de Veygo en **GitHub Pages**, siguiendo la configuración descrita en la sección 5.1.4. El sitio se publica desde la rama `main` del repositorio `landing-Page`, por lo que cada commit integrado en esa rama genera automáticamente una nueva publicación.

| Producto | Plataforma | Repositorio | Rama / carpeta | URL |
|:---|:---|:---|:---|:---|
| Landing Page | GitHub Pages | https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page | `main` / raíz | https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/ |

El despliegue se realizó con los siguientes pasos:

1. En **Settings → Pages** del repositorio, se configuró como origen **Deploy from a branch**, con la rama `main` y la carpeta raíz (`/root`).

![Configuración de GitHub Pages](assets/img/deploy-01-pages-settings.png)

2. Al registrar los commits del Sprint en `main`, GitHub ejecutó automáticamente el flujo **pages-build-deployment**, que construye y publica el sitio. Su ejecución puede revisarse en la pestaña **Actions** del repositorio.

![Ejecución de pages-build-deployment en GitHub Actions](assets/img/Pas03.png)

3. Al finalizar el flujo, GitHub Pages mostró el mensaje **"Your site is live"** con la URL pública de la Landing Page.

![Sitio publicado en GitHub Pages](assets/img/deploy-02-pages-actions.png)

4. Finalmente, se verificó el funcionamiento de la Landing Page desplegada en el navegador, comprobando el cambio de idioma, el buscador y los enlaces de navegación.

![Landing Page desplegada](assets/img/deploy-04-landing-live.png)


#### 5.2.1.8. Team Collaboration Insights during Sprint

Durante este Sprint, el equipo concentró sus actividades de implementación y colaboración en el desarrollo de la Landing Page. Para garantizar un trabajo ordenado y con trazabilidad, se utilizó Git como sistema de control de versiones sobre un repositorio público alojado en GitHub, bajo la organización 1ASI0729-2620-4399-G3-Veygo.

A continuación, se presentan las capturas de los analíticos de GitHub que evidencian la participación, los commits y los additions de todos los miembros del equipo durante este Sprint:

![aditions general](assets/img/Commits_sprint1.png)

![commits](assets/img/additions_sprint1_users.png)

### 5.2.2. Sprint 2
Para el segundo Sprint, el equipo se enfocó en implementar y desplegar la primera versión del **Frontend Web Application** de Veygo. La aplicación permite a los arrendatarios registrarse, buscar, reservar y calificar vehículos, guardar favoritos y comunicarse con los propietarios; y a los propietarios, publicar su flota, gestionar la disponibilidad, atender solicitudes y revisar sus ingresos y transacciones. La aplicación consume una Fake API (json-server) que simula los Web Services que se implementarán en el siguiente Sprint con ASP.NET Core.

A continuación, se presentan las historias de usuario seleccionadas para este Sprint:

| ID | User Story | Epic | Priority | SP |
| :-- | :-- | :-- | :-- | :-- |
| US37 | Registro de Usuario por Rol | EP-02 | High | 3 |
| US02 | Inicio de Sesión Seguro | EP-02 | High | 3 |
| US14 | Edición de Perfil de Usuario | EP-02 | Low | 2 |
| US03 | Búsqueda de Vehículos Cercanos | EP-03 | High | 5 |
| US38 | Detalle del Vehículo | EP-03 | High | 3 |
| US40 | Inicio del Arrendatario | EP-03 | Medium | 2 |
| US39 | Vehículos Favoritos | EP-03 | Low | 2 |
| US04 | Filtrado por Transmisión y Energía | EP-04 | High | 3 |
| US15 | Publicación de Nuevo Vehículo | EP-05 | High | 5 |
| US16 | Edición o Retiro de Publicación | EP-05 | Medium | 3 |
| US05 | Sincronización Automática de Disponibilidad | EP-06 | High | 5 |
| US17 | Solicitud de Reserva | EP-07 | High | 5 |
| US18 | Confirmación o Rechazo de Solicitud | EP-07 | High | 3 |
| US19 | Cancelación de Reserva | EP-07 | Medium | 3 |
| US20 | Historial de Reservas | EP-07 | Medium | 2 |
| US21 | Notificaciones de Actividad | EP-07 | Medium | 3 |
| US41 | Mensajería entre Cliente y Propietario | EP-07 | Medium | 5 |
| US06 | Métricas de Flota y Transacciones | EP-08 | Medium | 3 |
| US42 | Historial de Transacciones y Reporte | EP-08 | Medium | 3 |
| US07 | Evaluación Mutua Post-Alquiler | EP-09 | Medium | 3 |
| | | | **Total Story Points** | **66** |

#### 5.2.2.1. Sprint Planning 2.
La reunión de Sprint Planning 2 se realizó después de la revisión del Sprint 1. En ella el equipo revisó lo alcanzado con la Landing Page, acordó mejoras en la forma de trabajo y seleccionó las historias de usuario del Frontend Web Application que se implementarían en este Sprint.

| Campo | Detalle |
|---|---|
| **Sprint #** | Sprint 2 |
| **Fecha** | 2026-09-16 |
| **Hora** | 08:00 PM |
| **Lugar** | Reunión virtual vía Google Meet |
| **Preparado por** | Josue Antonio Flores Apaico |
| **Asistentes** | Josue Antonio Flores Apaico, Fabrizio Hamet Cano Ortiz, Marlon Alessandro Flores Siguas, Ivonne Beatriz Ibañez Torres y Eddo Su Caletti |
| **Resumen del Review del Sprint 1** | En el Sprint 1 se implementó y desplegó en GitHub Pages la primera versión de la Landing Page de Veygo, con navegación, selector de idioma (ES/EN), buscador rápido, categorías, vehículos destacados, sección de confianza y redirección al registro según el rol. Quedaron pendientes las secciones de preguntas frecuentes y suscripción a novedades. |
| **Resumen de la Retrospectiva del Sprint 1** | El equipo valoró la división del trabajo por archivos, pero identificó que los commits no siguieron siempre Conventional Commits y que se trabajó directamente sobre `main`. Para este Sprint se acordó aplicar GitFlow (ramas `feature/*` hacia `develop` mediante Pull Requests), usar Conventional Commits en inglés y organizar el código por bounded contexts. |
| **Objetivo del Sprint 2** | Nuestro enfoque está en entregar la primera versión del Frontend Web Application de Veygo, en la que el arrendatario puede registrarse, buscar, reservar y calificar vehículos, y el propietario puede publicar su flota, gestionar su disponibilidad, atender las solicitudes y revisar sus transacciones. Creemos que esto entrega a arrendatarios y propietarios de Lima un canal confiable para alquilar vehículos sin intermediarios informales. Esto se confirmará cuando un arrendatario complete una reserva y el propietario la confirme desde la aplicación desplegada, viendo ambos la notificación correspondiente. |
| **Velocity del Sprint 2** | 66 |
| **Suma de Story Points** | 66 |

#### 5.2.2.2. Aspect Leaders and Collaborators.
Los aspectos de este Sprint corresponden a los bounded contexts del Frontend Web Application, definidos en el Design-Level EventStorming (sección 4.6.1), además de la configuración base y el despliegue. Cada integrante lideró al menos un aspecto y colaboró en la revisión de los Pull Requests de los demás.

| Team Member | GitHub Username | IAM, Shared, i18n y Router | Fleet | Booking | Engagement | Communication | Dashboard | Payment, Reputation y Notification | Deployment (Render y Firebase) |
|---|---|---|---|---|---|---|---|---|---|
| **Flores Apaico, Josué Antonio** | **JosueFloresAp** | **L** | **L** | C | C | C | C | **L** | **L** |
| **Su Caletti, Eddo** | **Asalreon520** | C | C | **L** | C | C | C | C | C |
| **Ibañez Torres, Ivonne Beatriz** | **MarlonLasarte** | C | C | C | C | C | **L** | C | C |
| **Cano Ortiz, Fabrizio Hamet** | **Fabrizioco01** | C | C | C | C | **L** | C | C | C |
| **Flores Siguas, Marlon Alessandro** | **MarlonFS965** | C | C | C | **L** | C | C | C | C |

_(Nota: L = Leader, C = Collaborator)_

#### 5.2.2.3. Sprint Backlog 2

El objetivo principal de este Sprint fue implementar y desplegar la primera versión del Frontend Web Application de Veygo, organizada por bounded contexts y conectada a una Fake API desplegada. Las historias de usuario seleccionadas se descompusieron en tareas de entre 4 y 8 horas, que se gestionaron en Jira con los estados To Do, In Process, To Review y Done. Una tarea pasó a Done solo después de que su Pull Request fuera revisado e integrado a `develop`.

A continuación, se presenta una captura de pantalla del tablero de control para el Sprint 2:

![Tablero del Sprint 2 en Jira](assets/img/sprint2-board.png)

Enlace del Jira: https://josueflores9283.atlassian.net/jira/software/projects/SCRUM/boards/1?filter=&groupBy=none&atlOrigin=eyJpIjoiZDBjZGY3NGYwMDVkNDFjOTlkN2ZmNzZmOTUyM2YxZTQiLCJwIjoiaiJ9

| Sprint # | Sprint 2 | | | | | | |
|---|---|---|---|---|---|---|---|
| **Story Id** | **Story Title** | **Task Id** | **Task Title** | **Task Description** | **Estimation (Hours)** | **Assigned To** | **Status** |
| US37 | Registro de Usuario por Rol | T01 | Modelo de dominio y servicio de IAM | Implementar las entidades `User`, `UserRole`, `DriverLicense` y `UserPreferences`, además de `IamApi`, `UserAssembler`, el almacenamiento de sesión y el store de IAM. | 6 | Josué | Done |
| | | T02 | Vista de registro por rol | Implementar el registro con selección de rol (arrendatario o propietario), campos según el rol y validaciones. | 4 | Josué | Done |
| US02 | Inicio de Sesión Seguro | T03 | Inicio de sesión y guardas de navegación | Implementar la vista de inicio de sesión, la protección de rutas privadas y la separación de vistas por rol. | 5 | Josué | Done |
| US14 | Edición de Perfil de Usuario | T04 | Vista de perfil | Implementar la edición de datos personales, foto, licencia de conducir, preferencias y contraseña. | 4 | Josué | Done |
| US03 | Búsqueda de Vehículos Cercanos | T05 | Modelo y API de Fleet | Implementar `Vehicle`, `VehicleLocation`, `FleetApi`, `VehicleAssembler` y el store de Fleet. | 5 | Josué | Done |
| | | T06 | Búsqueda con mapa | Implementar la vista de búsqueda con mapa de OpenStreetMap (Leaflet) y tarjetas de vehículos con su precio. | 6 | Josué | Done |
| US38 | Detalle del Vehículo | T07 | Vista de detalle del vehículo | Implementar la galería, especificaciones, ubicación de recojo, datos del propietario y selección de fechas. | 4 | Josué | Done |
| US40 | Inicio del Arrendatario | T08 | Panel del arrendatario | Implementar el inicio del arrendatario con búsqueda rápida, categorías, recomendados, mapa y próximas reservas. | 4 | Ivonne | Done |
| US39 | Vehículos Favoritos | T09 | Contexto Engagement y favoritos | Implementar la entidad, la API y el store de favoritos, el botón de guardar y la vista de favoritos. | 4 | Marlon | Done |
| US04 | Filtrado por Transmisión y Energía | T10 | Filtros de catálogo | Implementar `VehicleSearchCriteria` (Specification) y el panel de filtros por precio, transmisión, combustible y calificación. | 4 | Josué | Done |
| US15 | Publicación de Nuevo Vehículo | T11 | Formulario de vehículo | Implementar el formulario con datos básicos, especificaciones, equipamiento, tarifas y carga de fotos. | 5 | Josué | Done |
| US16 | Edición o Retiro de Publicación | T12 | Gestión de flota | Implementar Mis vehículos, el detalle del propietario, la edición y la publicación o retiro de vehículos. | 4 | Josué | Done |
| US05 | Sincronización Automática de Disponibilidad | T13 | Calendario de disponibilidad | Implementar el calendario con días reservados, pendientes y bloqueados, y el bloqueo y desbloqueo de fechas. | 6 | Josué | Done |
| US17 | Solicitud de Reserva | T14 | Modelo y store de Booking | Implementar la entidad `Booking`, el assembler, la API y el store con la validación de disponibilidad. | 5 | Eddo | Done |
| | | T15 | Confirmación de reserva | Implementar la vista de confirmación con el resumen de días, precio, depósito y cálculo del total. | 4 | Eddo | Done |
| US18 | Confirmación o Rechazo de Solicitud | T16 | Solicitudes del propietario | Implementar la vista de reservas del propietario con aceptar y rechazar, y filtros por estado y vehículo. | 4 | Eddo | Done |
| US19 | Cancelación de Reserva | T17 | Cancelación de reservas | Implementar la cancelación desde las reservas del arrendatario y del propietario, con las reglas de cambio de estado. | 4 | Eddo | Done |
| US20 | Historial de Reservas | T18 | Mis reservas | Implementar la lista de reservas del arrendatario con filtro por estado y acceso a calificar los alquileres finalizados. | 4 | Eddo | Done |
| US21 | Notificaciones de Actividad | T19 | Contexto Notification y campana | Implementar la entidad, la API, el store, los handlers de eventos de dominio y la campana de notificaciones. | 6 | Josué | Done |
| US41 | Mensajería entre Cliente y Propietario | T20 | Mensajería | Implementar el contexto Communication con conversaciones y mensajes entre arrendatario y propietario. | 6 | Fabrizio | Done |
| US06 | Métricas de Flota y Transacciones | T21 | Panel del propietario | Implementar el inicio del propietario con métricas de vehículos, reservas, ingresos y calificación promedio. | 4 | Ivonne | Done |
| US42 | Historial de Transacciones y Reporte | T22 | Transacciones | Implementar el historial de transacciones por rango de fechas, los gráficos por mes y por vehículo, y la descarga del reporte CSV. | 5 | Josué | Done |
| US07 | Evaluación Mutua Post-Alquiler | T23 | Reseñas y reputación | Implementar el registro de reseñas y la vista de calificaciones con distribución de estrellas y nivel de reputación. | 5 | Josué | Done |
| — | Configuración base | T24 | Shared kernel, layout e i18n | Implementar `BaseApi`, `BaseEndpoint`, el error interceptor, los value objects compartidos, el layout y los idiomas EN/ES. | 6 | Josué | Done |
| — | Fake API | T25 | Fake API con json-server | Implementar la base de datos, las rutas con el prefijo `/api/v1` y los datos de prueba. | 4 | Josué | Done |
| — | Despliegue | T26 | Despliegue | Desplegar la Fake API en Render y la aplicación en Firebase Hosting con las variables de entorno de producción. | 4 | Josué | Done |

#### 5.2.2.4. Development Evidence for Sprint Review

Durante este Sprint se implementó la primera versión del Frontend Web Application de Veygo con Vue 3, JavaScript, PrimeVue, Vue Router, vue-i18n, Axios y Leaflet. El estado de cada bounded context se gestionó con stores basados en la API de reactividad de Vue (`reactive`). El código se organizó por bounded contexts (IAM, Fleet, Booking, Engagement, Reputation, Payment, Communication, Notification y Dashboard), cada uno con sus capas domain, application, infrastructure y presentation, además de un contexto `shared` con los elementos comunes.

El equipo aplicó GitFlow: cada funcionalidad se desarrolló en su propia rama `feature/*`, que se integró a `develop` mediante Pull Requests (#1 al #14). Finalmente, `develop` se integró a `main` mediante el Pull Request #15 para el despliegue. La mayoría de los commits siguen la convención Conventional Commits (`tipo(alcance): descripción`). Algunos commits de las ramas `feature/booking` y `feature/dashboard` no respetaron este formato. Para el siguiente Sprint, la convención se aplicará en todos los commits.

Repositorio del Frontend Web Application: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend

A continuación, se presentan los commits más representativos de cada bounded context. El historial completo se encuentra en el enlace al final de esta sección.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| 1ASI0729-2620-4399-G3-Veygo/frontend | main | f68ef1f | chore: initial commit | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 218489a | feat(api): add base api and base endpoint | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 2e4202c | feat(shared): add domain event bus | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 6e618e4 | feat(ui): add layout, top bar, navigation menu, footer and language switcher | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/i18n | 37aac26 | chore(i18n): add vue-i18n configuration | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | 18f32cb | feat(iam): add user entity, user role, driver license and preferences | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | 6dfdd4b | feat(iam): add sign-in, sign-up and profile views | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/router | 63df29b | feat(router): add routes and role-based navigation guard | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | d8e5c0c | feat(fleet): add vehicle entity, value objects and search criteria | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/fleet | e58e8a0 | feat(fleet): add vehicle search, detail, form and availability views | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 6fa347d | add Booking domain entity with validation, pricing, and lifecycle methods | — | Eddo Su Caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 6ebf174 | feat(booking): implement booking store with availability validation and status lifecycle actions. | — | Eddo Su Caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/booking | 04cbdc0 | implement booking confirmation view, owner requests dashboard, and renter bookings list | — | Eddo Su Caletti | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | c8aad59 | feat(engagement): add favorite entity | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/engagement | 43690c7 | feat(engagement): add favorite vehicles view | — | Marlon Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | 2bfc308 | feat(communication): add conversation entity | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/communication | cf2d1e8 | feat(communication): add messages view | — | Fabrizio Cano | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/dashboard | 3b23a82 | FEATURE(dashboard):owner-home | — | Ivonne Ibañez | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/dashboard | 10473d4 | FEATURE(dashboard):renter-home | — | Ivonne Ibañez | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/reputation | 1a5b01e | feat(reputation): add owner ratings view | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/payment | 85e8f1b | feat(payment): add transaction entity and income summary | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/notification | 20a50b1 | feat(notification): add notification entity | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | b7b0e93 | feat(fake-api): add json-server database and routes | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | main | db4889c | feat(firebase): add firebase hosting configuration | — | Josué Flores | 05/10/2026 |

_(Los commits no incluyen un cuerpo de mensaje; la descripción del cambio está en el título del commit.)_

Enlace del historial de commits: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/commits/main

Enlace de los Pull Requests: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/pulls?q=is%3Apr+is%3Aclosed

#### 5.2.2.5. Execution Evidence for Sprint Review

Al término del Sprint 2, el equipo implementó y desplegó la primera versión del Frontend Web Application de Veygo. La aplicación ofrece dos experiencias según el rol del usuario: el arrendatario puede buscar vehículos por ubicación, fechas y tipo, revisar su detalle, reservarlos, guardarlos como favoritos, calificar sus alquileres y conversar con el propietario; el propietario puede publicar y editar vehículos, gestionar su disponibilidad, aceptar o rechazar solicitudes y revisar sus transacciones y calificaciones. Ambos roles reciben notificaciones sobre el estado de sus reservas y los mensajes nuevos. La interfaz está disponible en inglés (idioma por defecto) y en español.

Link de la aplicación: https://veygo-web-app.web.app

Link del video: https://drive.google.com/file/d/1PieO7ejladIV7ItzjTtMbdd-lqVBScS3/view?usp=sharing

Cuentas de prueba (contraseña `Veygo2026!`): `leo.ramos@veygo.pe` (arrendatario) y `laura.torres@veygo.pe` (propietario).

| User Story | Evidencia |
|---|---|
| US37, US02 | Registro por rol e inicio de sesión |
| US40, US03, US04 | Inicio del arrendatario, búsqueda con mapa y filtros |
| US38, US17 | Detalle del vehículo y confirmación de reserva |
| US20, US19 | Historial y cancelación de reservas |
| US39 | Vehículos favoritos |
| US41, US21 | Mensajería y notificaciones |
| US14 | Perfil del usuario |
| US06 | Inicio del propietario con métricas |
| US15, US16 | Publicación, edición y retiro de vehículos |
| US05 | Calendario de disponibilidad |
| US18 | Aceptación o rechazo de solicitudes |
| US42 | Transacciones y reporte |
| US07 | Calificaciones y reseñas |

<h4>Inicio de sesión y registro</h4>

![Inicio de sesión](assets/img/sprint2/exec-01-sign-in.png)

**US02.** Vista de inicio de sesión con el formulario sobre una escena animada de carretera nocturna y selector de idioma.

![Registro](assets/img/sprint2/exec-02-sign-up.png)

**US37.** Registro con selección de rol (arrendatario o propietario). Los campos cambian según el rol elegido y el mensaje de la derecha se adapta al tipo de usuario.

<h4>Arrendatario: inicio y búsqueda</h4>

![Inicio del arrendatario](assets/img/sprint2/exec-03-renter-home.png)

**US40.** Inicio del arrendatario con buscador por ubicación, fecha de inicio, fecha fin y tipo de vehículo, accesos por categoría, vehículos recomendados, mapa de vehículos cercanos y próximas reservas.

![Búsqueda de vehículos](assets/img/sprint2/exec-04-vehicle-search.png)

**US03 y US04.** Búsqueda con filtros por precio, transmisión, combustible y calificación, resultados disponibles en las fechas elegidas y mapa de OpenStreetMap con el precio de cada vehículo.

<h4>Arrendatario: detalle y reserva</h4>

![Detalle del vehículo](assets/img/sprint2/exec-05-vehicle-detail.png)

**US38.** Detalle del vehículo con galería, especificaciones, ubicación de recojo, datos del propietario y selección de fechas.

![Confirmación de reserva](assets/img/sprint2/exec-06-booking-confirmation.png)

**US17.** Confirmación de la reserva con el resumen de días, precio y depósito. Antes de crearla, el sistema verifica que las fechas no se crucen con otra reserva o con días bloqueados.

![Mis reservas](assets/img/sprint2/exec-07-renter-bookings.png)

**US20 y US19.** Historial de reservas filtrable por estado, con opciones para cancelar y calificar los alquileres finalizados.

![Favoritos](assets/img/sprint2/exec-08-favorites.png)

**US39.** Vehículos guardados como favoritos.

<h4>Comunicación, notificaciones y perfil</h4>

![Mensajes](assets/img/sprint2/exec-09-messages.png)

**US41.** Mensajería entre arrendatario y propietario.

![Notificaciones](assets/img/sprint2/exec-10-notifications.png)

**US21.** Campana de notificaciones con los cambios de estado de las reservas y los mensajes nuevos.

![Perfil](assets/img/sprint2/exec-11-profile.png)

**US14.** Perfil del usuario con datos personales, licencia de conducir, estadísticas y preferencias de idioma, notificaciones y modo oscuro.

<h4>Propietario: inicio y flota</h4>

![Inicio del propietario](assets/img/sprint2/exec-12-owner-home.png)

**US06.** Inicio del propietario con métricas de vehículos, próximas reservas, ingresos del mes y calificación promedio, junto con accesos rápidos.

![Mis vehículos](assets/img/sprint2/exec-13-owner-vehicles.png)

**US16.** Gestión de la flota: búsqueda, filtros, publicación o retiro, edición y detalle de cada vehículo.

![Detalle del vehículo para el propietario](assets/img/sprint2/exec-14-owner-vehicle-detail.png)

**US16.** Detalle del vehículo desde la perspectiva del propietario, con precios, información adicional, disponibilidad y estadísticas.

![Agregar vehículo](assets/img/sprint2/exec-15-vehicle-form.png)

**US15.** Formulario de publicación con datos básicos, especificaciones, equipamiento, información adicional y carga de fotos.

<h4>Propietario: disponibilidad, reservas, transacciones y calificaciones</h4>

![Disponibilidad](assets/img/sprint2/exec-16-availability.png)

**US05.** Calendario de disponibilidad por vehículo con días reservados, pendientes y bloqueados, y acciones para bloquear o desbloquear fechas.

![Reservas del propietario](assets/img/sprint2/exec-17-owner-bookings.png)

**US18.** Solicitudes de reserva con opciones para aceptar o rechazar, y filtros por estado y vehículo.

![Transacciones](assets/img/sprint2/exec-18-transactions.png)

**US42.** Transacciones con rango de fechas editable, resumen de ingresos, gráfico por mes y por vehículo, historial y descarga del reporte.

![Calificaciones](assets/img/sprint2/exec-19-ratings.png)

**US07.** Calificaciones con el promedio, la distribución de estrellas, las reseñas de los clientes y la calificación por vehículo.

#### 5.2.2.6. Services Documentation Evidence for Sprint Review

En este Sprint no se implementaron los Web Services en ASP.NET Core; están planificados para el siguiente Sprint, donde se documentarán con OpenAPI (Swagger). Para que el Frontend Web Application funcione con datos persistentes, el equipo implementó una **Fake API** con json-server, que expone los recursos REST que tendrá la API definitiva bajo el prefijo `/api/v1`. El prefijo se configuró en `routes.json` (`"/api/v1/*": "/$1"`), y la Fake API está desplegada en Render.

URL base: https://veygo-fake-api.onrender.com/api/v1

Repositorio (carpeta `server/`): https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/tree/main/server

Todas las llamadas se realizan desde la capa de infraestructura de cada bounded context (`*-api.js`), que extiende las clases compartidas `BaseApi` y `BaseEndpoint`. Las listas usan además los parámetros de json-server `_sort`, `_order` y `_limit` para ordenar y limitar los resultados.

| Recurso | Endpoint | Acciones utilizadas | Sintaxis de llamada | Parámetros | Uso en la aplicación |
|---|---|---|---|---|---|
| Users | `/users` | GET, POST, PATCH, DELETE | `GET /api/v1/users?email={email}&password={password}` <br> `GET /api/v1/users?email={email}` <br> `GET /api/v1/users/{id}` <br> `POST /api/v1/users` <br> `PATCH /api/v1/users/{id}` <br> `DELETE /api/v1/users/{id}` | `email`, `password`, `id`, body con los datos del usuario | Inicio de sesión, validación de correo duplicado, registro, edición de perfil y contraseña, y eliminación de cuenta. |
| Vehicles | `/vehicles` | GET, POST, PUT, PATCH, DELETE | `GET /api/v1/vehicles?published=true` <br> `GET /api/v1/vehicles?ownerId={id}` <br> `GET /api/v1/vehicles/{id}` <br> `POST /api/v1/vehicles` <br> `PUT /api/v1/vehicles/{id}` <br> `PATCH /api/v1/vehicles/{id}` <br> `DELETE /api/v1/vehicles/{id}` | `published`, `ownerId`, `id`, body con los datos del vehículo | Catálogo, búsqueda, detalle, publicación, edición, publicar o retirar y eliminación de vehículos. |
| Blocked dates | `/blockedDates` | GET, POST, DELETE | `GET /api/v1/blockedDates?vehicleId={id}` <br> `POST /api/v1/blockedDates` <br> `DELETE /api/v1/blockedDates/{id}` | `vehicleId`, `id` | Bloqueo y desbloqueo de fechas en el calendario de disponibilidad. |
| Bookings | `/bookings` | GET, POST, PATCH | `GET /api/v1/bookings?renterId={id}` <br> `GET /api/v1/bookings?ownerId={id}` <br> `GET /api/v1/bookings?vehicleId={id}` <br> `POST /api/v1/bookings` <br> `PATCH /api/v1/bookings/{id}` | `renterId`, `ownerId`, `vehicleId`, `id`, body con el nuevo estado | Solicitud, confirmación, rechazo, cancelación e historial de reservas, y cálculo de transacciones e ingresos. |
| Favorites | `/favorites` | GET, POST, DELETE | `GET /api/v1/favorites?renterId={id}` <br> `POST /api/v1/favorites` <br> `DELETE /api/v1/favorites/{id}` | `renterId`, `id` | Guardar y quitar vehículos favoritos. |
| Reviews | `/reviews` | GET, POST | `GET /api/v1/reviews?vehicleId={id}` <br> `GET /api/v1/reviews?ownerId={id}` <br> `POST /api/v1/reviews` | `vehicleId`, `ownerId` | Registro de reseñas y cálculo de la reputación. |
| Conversations | `/conversations` | GET, POST, PATCH | `GET /api/v1/conversations?renterId={id}` <br> `GET /api/v1/conversations?ownerId={id}` <br> `POST /api/v1/conversations` <br> `PATCH /api/v1/conversations/{id}` | `renterId`, `ownerId`, `id` | Lista de conversaciones y actualización del último mensaje. |
| Messages | `/messages` | GET, POST, PATCH | `GET /api/v1/messages?conversationId={id}` <br> `POST /api/v1/messages` <br> `PATCH /api/v1/messages/{id}` | `conversationId`, `id` | Envío de mensajes y marcado como leídos. |
| Notifications | `/notifications` | GET, POST, PATCH | `GET /api/v1/notifications?userId={id}` <br> `POST /api/v1/notifications` <br> `PATCH /api/v1/notifications/{id}` | `userId`, `id` | Campana de notificaciones y marcado como leídas. |

El bounded context Payment no tiene un endpoint propio en la Fake API: las transacciones y el resumen de ingresos se calculan en el frontend a partir de las reservas confirmadas y completadas.

> **Nota:** en la Fake API, el inicio de sesión se resuelve con una consulta `GET` por correo y contraseña, porque json-server no ofrece autenticación. En los Web Services del siguiente Sprint, este flujo se reemplazará por `POST /api/v1/authentication/sign-in`, con contraseñas cifradas mediante BCrypt y un token JWT, según lo definido en el Capítulo IV.

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

La respuesta devuelve la reserva con los identificadores del vehículo, el arrendatario y el propietario, el periodo de alquiler, el precio y el estado (`pending`, `confirmed`, `rejected`, `cancelled` o `completed`).

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

![Fake API desplegada](assets/img/fake-api-vehicles.png)

Respuesta de `GET /api/v1/vehicles` desde la Fake API desplegada en Render.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/iam | ab370f8 | build: add leaflet and json-server dependencies | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | 218489a | feat(api): add base api and base endpoint | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/shared | f762ef5 | feat(api): add error interceptor | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | b7b0e93 | feat(fake-api): add json-server database and routes | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | ffdd01d | build: add fake-api script | — | Josué Flores | 05/10/2026 |
| 1ASI0729-2620-4399-G3-Veygo/frontend | feature/app-setup | 9972fed | fix(build): move fake-api script into scripts section | — | Josué Flores | 05/10/2026 |

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

Durante este Sprint el equipo trabajó en el repositorio `frontend` de la organización 1ASI0729-2620-4399-G3-Veygo aplicando GitFlow. Cada integrante desarrolló su bounded context en una rama `feature/*` y la integró a `develop` mediante un Pull Request; finalmente, `develop` se integró a `main` mediante el Pull Request #15 para el despliegue.

El repositorio registra 89 commits en la rama `main`: 75 commits de desarrollo y 14 commits de merge generados al integrar los Pull Requests. La siguiente tabla resume los commits de desarrollo de cada integrante:

| Integrante | Cuenta(s) de GitHub | Rama(s) | Pull Request(s) | Commits |
|---|---|---|---|---|
| Flores Apaico, Josué Antonio | JosueFloresAp | feature/fleet, feature/iam, feature/i18n, feature/notification, feature/payment, feature/reputation, feature/router, feature/shared, feature/app-setup | #1, #3, #4, #5, #6, #7, #8, #9, #14 y #15 | 40 |
| Su Caletti, Eddo | Asaltron520 / Eddo Su caletti | feature/booking | #10 | 16 |
| Cano Ortiz, Fabrizio Hamet | Fabrizioco01 | feature/communication | #12 | 10 |
| Flores Siguas, Marlon Alessandro | MarlonFS965 | feature/engagement | #11 | 6 |
| Ibañez Torres, Ivonne Beatriz | MarlonLasarte | feature/dashboard | #13 | 3 |
| | | | **Total** | **75** |

_(Nota: Eddo Su Caletti realizó commits desde dos configuraciones de Git distintas, por lo que GitHub los muestra con dos nombres. La cuenta `MarlonLasarte` pertenece a Ivonne Ibañez.)_

La carga de commits no fue equilibrada: Josué Flores concentró la configuración base, los contextos compartidos y el despliegue. Para el siguiente Sprint, el equipo acordó distribuir los bounded contexts del backend de forma más equitativa.

A continuación, se presentan las capturas de los analíticos de GitHub que evidencian la participación de los miembros del equipo durante este Sprint:

![Contributors](assets/img/insights-contributors.png)

Contribuciones por integrante en el repositorio `frontend`.

![Commits](assets/img/insights-commits.png)

Actividad de commits durante el Sprint.

![Network](assets/img/insights-network.png)

Gráfico de red con las ramas `feature/*` integradas a `develop` y `main`.

![Pulse](assets/img/pulse.png)


### 5.2.3. Sprint 3
Para el tercer Sprint, el equipo se enfocó en implementar y desplegar la primera versión de los **RESTful Web Services** de Veygo con ASP.NET Core, Entity Framework Core y MySQL, documentados con OpenAPI (Swagger). Los Web Services reemplazan a la Fake API utilizada en el Sprint 2 y exponen los recursos de autenticación, vehículos, disponibilidad, reservas, favoritos, mensajería, notificaciones, perfil, métricas y reseñas, organizados por bounded contexts. Además, se desplegó una nueva versión del Frontend Web Application conectada a los Web Services, con autenticación mediante JWT, y una nueva versión de la Landing Page que completa las secciones pendientes del Sprint 1 e incorpora el Video About-the-Product.

A continuación, se presentan las historias de usuario y technical stories seleccionadas para este Sprint:

| ID | User Story / Technical Story | Epic | Priority | SP |
| :-- | :-- | :-- | :-- | :-- |
| TS25 | Endpoint de Registro y Autenticación | EP-02 | High | 5 |
| TS54 | Endpoints de Perfil | EP-02 | Medium | 3 |
| US43 | Cierre de Sesión | EP-02 | Medium | 1 |
| TS27 | Endpoint de Búsqueda Geolocalizada | EP-03 | High | 5 |
| TS51 | Endpoints de Favoritos | EP-03 | Low | 3 |
| TS28 | Endpoint de Filtros de Catálogo | EP-04 | High | 3 |
| TS29 | Endpoints CRUD de Publicación de Vehículos | EP-05 | High | 8 |
| TS30 | Endpoint de Calendario de Disponibilidad | EP-06 | High | 5 |
| TS31 | Endpoints de Solicitud y Confirmación de Reserva | EP-07 | High | 8 |
| TS52 | Endpoints de Conversaciones y Mensajes | EP-07 | Medium | 5 |
| TS53 | Endpoints de Notificaciones | EP-07 | Medium | 3 |
| TS32 | Endpoint de Métricas del Propietario | EP-08 | Medium | 5 |
| TS33 | Endpoint de Calificaciones y Reseñas | EP-09 | Medium | 5 |
| TS57 | Documentación de la API con OpenAPI | Transversal | High | 3 |
| US23 | Sección de Preguntas Frecuentes | EP-01 | Low | 1 |
| US24 | Suscripción a Novedades | EP-01 | Low | 2 |
| | | | **Total Story Points** | **65** |


#### 5.2.3.1. Sprint Planning 3.
La reunión de Sprint Planning 3 se realizó después de la revisión del Sprint 2. En ella el equipo revisó lo alcanzado con el Frontend Web Application, analizó las observaciones de la retrospectiva y seleccionó las technical stories de los Web Services y las historias de usuario de la Landing Page que se implementarían en este Sprint.

| Campo | Detalle |
|---|---|
| **Sprint #** | Sprint 3 |
| **Fecha** | 2026-10-23 |
| **Hora** | 08:00 PM |
| **Lugar** | Reunión virtual vía Google Meet |
| **Preparado por** | Josue Antonio Flores Apaico |
| **Asistentes** | Josue Antonio Flores Apaico, Fabrizio Hamet Cano Ortiz, Marlon Alessandro Flores Siguas, Ivonne Beatriz Ibañez Torres y Eddo Su Caletti |
| **Resumen del Review del Sprint 2** | En el Sprint 2 se implementó y desplegó en Firebase Hosting la primera versión del Frontend Web Application de Veygo, con 20 historias de usuario (66 story points). El arrendatario puede registrarse, buscar vehículos en un mapa, filtrarlos, reservarlos, guardarlos como favoritos, calificar sus alquileres y comunicarse con el propietario; el propietario puede publicar y gestionar su flota, controlar la disponibilidad, atender solicitudes y revisar sus métricas, transacciones y calificaciones. La aplicación consume una Fake API con json-server desplegada en Render, que define los contratos REST que tendrán los Web Services. |
| **Resumen de la Retrospectiva del Sprint 2** | El equipo valoró la organización del código por bounded contexts y el uso de GitFlow con Pull Requests, que permitieron trabajar en paralelo sin conflictos. Como oportunidades de mejora, identificó que la carga de trabajo no se distribuyó de forma equilibrada, que algunos commits no siguieron Conventional Commits y que el inicio de sesión de la Fake API enviaba la contraseña en la URL. Para este Sprint se acordó asignar a cada integrante al menos un bounded context de los Web Services y una tarea de integración en el frontend, revisar la convención de commits en cada Pull Request y aplicar autenticación con JWT y contraseñas cifradas con BCrypt. |
| **Objetivo del Sprint 3** | Nuestro enfoque está en entregar la primera versión de los Web Services de Veygo y conectar el Frontend Web Application a ellos, reemplazando la Fake API. Creemos que esto entrega a arrendatarios y propietarios una plataforma segura y confiable, en la que sus cuentas, vehículos y reservas se almacenan de forma persistente y protegida. Esto se confirmará cuando un arrendatario inicie sesión con un token JWT, cree una reserva desde la aplicación desplegada, el propietario la confirme y ambos operaciones queden registradas en la base de datos MySQL y documentadas en Swagger. |
| **Velocity del Sprint 3** | 66 |
| **Suma de Story Points** | 65 |


#### 5.2.3.2. Aspect Leaders and Collaborators.
Los aspectos de este Sprint corresponden a los bounded contexts de los Web Services definidos en el Capítulo IV, además de la nueva versión de la Landing Page, la configuración transversal (shared kernel, internacionalización y documentación con OpenAPI) y el despliegue. A diferencia del Sprint 2, la carga se distribuyó de forma equilibrada: cada integrante lideró al menos un bounded context de los Web Services, se encargó de integrarlo en el Frontend Web Application y participó en la nueva versión de la Landing Page. Además, colaboró en la revisión de los Pull Requests de los demás.

| Team Member | GitHub Username | IAM y Perfil | Fleet | Availability y Booking | Engagement, Communication y Notification | Reputation y Dashboard | Landing Page | Shared, i18n y OpenAPI | Deployment (Web Services, Web App y Landing) |
|---|---|---|---|---|---|---|---|---|---|
| **Flores Apaico, Josué Antonio** | **JosueFloresAp** | **L** | C | C | C | C | C | **L** | **L** |
| **Flores Siguas, Marlon Alessandro** | **MarlonFS965** | C | **L** | C | C | C | C | C | C |
| **Su Caletti, Eddo** | **Asalreon520** | C | C | **L** | C | C | C | C | C |
| **Cano Ortiz, Fabrizio Hamet** | **Fabrizioco01** | C | C | C | **L** | C | C | C | C |
| **Ibañez Torres, Ivonne Beatriz** | **MarlonLasarte** | C | C | C | C | **L** | **L** | C | C |

_(Nota: L = Leader, C = Collaborator)_


#### 5.2.3.3. Sprint Backlog 3.

El objetivo principal de este Sprint fue implementar y desplegar la primera versión de los Web Services de Veygo, conectar a ellos el Frontend Web Application y publicar una nueva versión de la Landing Page con las secciones pendientes, atributos de accesibilidad (ARIA) e internacionalización en inglés y español latinoamericano. Las historias seleccionadas se descompusieron en tareas de entre 4 y 8 horas, gestionadas en Jira con los estados To Do, In Process, To Review y Done. Una tarea pasó a Done solo después de que su Pull Request fuera revisado e integrado a `develop`.

A continuación, se presenta una captura de pantalla del tablero de control para el Sprint 3:

![Tablero del Sprint 3 en Jira](assets/img/sprint3-board.png)

Enlace del Jira: https://josueflores9283.atlassian.net/jira/software/projects/SCRUM/boards/1

| Sprint # | Sprint 3 | | | | | | |
|---|---|---|---|---|---|---|---|
| **Story Id** | **Story Title** | **Task Id** | **Task Title** | **Task Description** | **Estimation (Hours)** | **Assigned To** | **Status** |
| TS57 | Documentación de la API con OpenAPI | T01 | Esqueleto de los Web Services | Crear el proyecto ASP.NET Core organizado por bounded contexts, el shared kernel (entidad base, repositorio base, Unit of Work y AppDbContext con convención snake_case) y la conexión a MySQL con Entity Framework Core. | 8 | Josué | To Do |
|  |  | T02 | OpenAPI e internacionalización | Configurar Swagger con la documentación de los endpoints y la internacionalización de los mensajes de la API en inglés (por defecto) y español latinoamericano (es-419). | 6 | Josué | To Do |
| TS25 | Endpoint de Registro y Autenticación | T03 | Modelo de dominio de IAM | Implementar el agregado User con su rol, el cifrado de contraseñas con BCrypt y el servicio de generación y validación de tokens JWT. | 8 | Josué | To Do |
|  |  | T04 | Endpoints de autenticación | Implementar sign-up y sign-in, el middleware de autorización por token y los recursos y assemblers de IAM. | 6 | Josué | To Do |
| TS54 | Endpoints de Perfil | T05 | Endpoints de perfil | Implementar la consulta y edición del perfil, el cambio de contraseña y la eliminación de la cuenta. | 5 | Fabrizio | To Do |
| US43 | Cierre de Sesión | T06 | Integración de IAM en el frontend | Reemplazar el inicio de sesión de la Fake API por los endpoints de IAM, enviar el token en el encabezado Authorization e implementar el cierre de sesión. | 5 | Josué | To Do |
| TS29 | Endpoints CRUD de Publicación de Vehículos | T07 | Modelo de dominio de Fleet | Implementar el agregado Vehicle con sus value objects, el repositorio y la configuración de Entity Framework Core. | 8 | Marlon | To Do |
|  |  | T08 | Endpoints CRUD de vehículos | Implementar la creación, consulta por id y por propietario, edición, publicación o retiro y eliminación de vehículos. | 8 | Marlon | To Do |
|  |  | T09 | Integración de Fleet en el frontend | Conectar la búsqueda, el detalle y la gestión de flota a los endpoints de Fleet y ajustar los assemblers. | 5 | Marlon | To Do |
| TS27 | Endpoint de Búsqueda Geolocalizada | T10 | Búsqueda geolocalizada | Implementar la consulta de vehículos publicados cercanos a una ubicación y disponibles en un rango de fechas. | 6 | Marlon | To Do |
| TS28 | Endpoint de Filtros de Catálogo | T11 | Filtros de catálogo | Implementar los filtros por tipo, transmisión, combustible, precio y calificación en la consulta de vehículos. | 5 | Marlon | To Do |
| TS30 | Endpoint de Calendario de Disponibilidad | T12 | Endpoints de disponibilidad | Implementar la consulta, el bloqueo y el desbloqueo de fechas, con la validación de cruces con reservas confirmadas. | 6 | Eddo | To Do |
| TS31 | Endpoints de Solicitud y Confirmación de Reserva | T13 | Modelo de dominio de Booking | Implementar el agregado Booking con el cálculo del total, la validación de disponibilidad y las transiciones de estado. | 8 | Eddo | To Do |
|  |  | T14 | Endpoints de reservas | Implementar la creación de reservas, la consulta por arrendatario, propietario y vehículo, y la confirmación, rechazo, cancelación y finalización. | 8 | Eddo | To Do |
|  |  | T15 | Integración de Booking en el frontend | Conectar la reserva, el historial, las solicitudes del propietario y el calendario de disponibilidad a los Web Services. | 5 | Eddo | To Do |
| TS52 | Endpoints de Conversaciones y Mensajes | T16 | Endpoints de mensajería | Implementar las entidades Conversation y Message y los endpoints para listar conversaciones, enviar mensajes y marcarlos como leídos. | 8 | Fabrizio | To Do |
|  |  | T17 | Integración de Engagement, Communication y Notification | Conectar favoritos, mensajería y la campana de notificaciones a los Web Services. | 5 | Fabrizio | To Do |
| TS53 | Endpoints de Notificaciones | T18 | Endpoints de notificaciones | Implementar la entidad Notification, sus endpoints y la creación automática ante cambios de estado de reservas y mensajes nuevos. | 6 | Fabrizio | To Do |
| TS51 | Endpoints de Favoritos | T19 | Endpoints de favoritos | Implementar la consulta, el registro y la eliminación de vehículos favoritos del arrendatario. | 4 | Fabrizio | To Do |
| TS33 | Endpoint de Calificaciones y Reseñas | T20 | Endpoints de reseñas | Implementar la entidad Review, el registro de reseñas, la consulta por vehículo y propietario y el resumen de reputación. | 6 | Ivonne | To Do |
| TS32 | Endpoint de Métricas del Propietario | T21 | Endpoint de métricas del propietario | Implementar las métricas de vehículos activos, reservas, ingresos del mes, calificación promedio y transacciones por rango de fechas. | 8 | Ivonne | To Do |
|  |  | T22 | Integración de Dashboard y Reputation | Conectar el inicio del propietario, las transacciones y las calificaciones a los Web Services. | 5 | Ivonne | To Do |
| US23 | Sección de Preguntas Frecuentes | T23 | Sección de preguntas frecuentes | Implementar la sección de preguntas frecuentes de la Landing Page en inglés y español, con atributos ARIA. | 4 | Ivonne | To Do |
| US24 | Suscripción a Novedades | T24 | Suscripción a novedades | Implementar el formulario de suscripción con validación del correo y mensaje de confirmación. | 4 | Ivonne | To Do |
| — | Accesibilidad e i18n de la Landing Page | T25 | Accesibilidad de navegación y selector de idioma | Agregar atributos ARIA y textos en es-419 en el encabezado, el menú y el selector de idioma de la Landing Page. | 4 | Josué | To Do |
| — | Accesibilidad e i18n de la Landing Page | T26 | Accesibilidad de categorías y destacados | Agregar atributos ARIA y textos en es-419 en las secciones de categorías y vehículos destacados de la Landing Page. | 4 | Marlon | To Do |
| — | Accesibilidad e i18n de la Landing Page | T27 | Accesibilidad del buscador y proceso | Agregar atributos ARIA y textos en es-419 en el buscador rápido y la sección Cómo funciona de la Landing Page. | 4 | Eddo | To Do |
| — | Accesibilidad e i18n de la Landing Page | T28 | Accesibilidad de confianza y testimonios | Agregar atributos ARIA y textos en es-419 en las secciones de confianza y testimonios de la Landing Page. | 4 | Fabrizio | To Do |
| — | Despliegue | T29 | Despliegue de los Web Services | Crear la base de datos MySQL en la nube, desplegar los Web Services y configurar las variables de entorno y CORS. | 6 | Josué | To Do |
| — | Despliegue | T30 | Despliegue de la Web App y la Landing Page | Apuntar el Frontend Web Application a los Web Services desplegados, incrustar el Video About-the-Product en la Landing Page y publicar ambas versiones. | 4 | Ivonne | To Do |

#### 5.2.3.4. Development Evidence for Sprint Review.

Durante este Sprint se implementó la primera versión de los RESTful Web Services de Veygo con ASP.NET Core, Entity Framework Core y MySQL, utilizando C# como lenguaje de programación. El código se organizó por bounded contexts (IAM, Fleet, Booking, Engagement, Communication, Notification, Reputation y Dashboard), cada uno con sus capas Domain, Application, Infrastructure e Interfaces, además de un contexto Shared con los elementos comunes. La autenticación se implementó con tokens JWT y contraseñas cifradas con BCrypt, y la documentación de los endpoints con OpenAPI (Swagger).

Asimismo, se integró el Frontend Web Application con los Web Services, reemplazando la Fake API, y se publicó una nueva versión de la Landing Page con las secciones de preguntas frecuentes y suscripción a novedades, atributos ARIA e internacionalización en inglés y español latinoamericano.

El equipo aplicó GitFlow en los tres repositorios: cada funcionalidad se desarrolló en una rama `feature/*`, integrada a `develop` mediante Pull Requests, y luego `develop` se integró a `main` para el despliegue. Todos los commits siguieron la convención Conventional Commits, y cada versión publicada se identificó con un tag de Semantic Versioning.

Repositorios:
- Web Services: https://github.com/1ASI0729-2620-4399-G3-Veygo/backend
- Frontend Web Application: https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend
- Landing Page: https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page

A continuación, se presentan los commits más representativos de cada producto:

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| (se completa con los commits reales) | | | | | | |

Enlaces del historial de commits:
- https://github.com/1ASI0729-2620-4399-G3-Veygo/backend/commits/main
- https://github.com/1ASI0729-2620-4399-G3-Veygo/frontend/commits/main
- https://github.com/1ASI0729-2620-4399-G3-Veygo/landing-Page/commits/main


#### 5.2.3.5. Execution Evidence for Sprint Review.

Al término del Sprint 3, el equipo desplegó la primera versión de los Web Services de Veygo y conectó a ellos el Frontend Web Application, que dejó de utilizar la Fake API. Los usuarios ahora se registran e inician sesión con contraseñas cifradas y un token JWT, y toda la información de vehículos, disponibilidad, reservas, favoritos, mensajes, notificaciones y reseñas se almacena de forma persistente en una base de datos MySQL. Además, se publicó una nueva versión de la Landing Page con las secciones de preguntas frecuentes y suscripción a novedades, atributos de accesibilidad (ARIA) y soporte para inglés (idioma por defecto) y español latinoamericano.

Link de la Landing Page: https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/

Link de la aplicación: https://veygo-web-app.web.app

Link del video: https://drive.google.com/file/d/XXXXXXXX/view?usp=sharing

| User Story / Technical Story | Evidencia |
|---|---|
| US23, US24 | Nuevas secciones de la Landing Page |
| TS25, US43 | Registro, inicio y cierre de sesión con JWT |
| TS27, TS28 | Búsqueda geolocalizada y filtros desde los Web Services |
| TS29 | Publicación y gestión de vehículos persistida |
| TS30, TS31 | Disponibilidad y ciclo de vida de la reserva |
| TS51, TS52, TS53 | Favoritos, mensajería y notificaciones |
| TS32, TS33 | Métricas del propietario y reseñas |
| TS54 | Edición de perfil y cambio de contraseña |

<h4>Landing Page</h4>

![Preguntas frecuentes](assets/img/sprint3/exec-01-landing-faq.png)

**US23.** Sección de preguntas frecuentes con respuestas desplegables, disponible en inglés y español.

![Suscripción a novedades](assets/img/sprint3/exec-02-landing-subscribe.png)

**US24.** Formulario de suscripción a novedades con validación del correo y mensaje de confirmación.

<h4>Autenticación con los Web Services</h4>

![Inicio de sesión con JWT](assets/img/sprint3/exec-03-sign-in-jwt.png)

**TS25.** Inicio de sesión contra los Web Services. En las herramientas de desarrollo del navegador se observa la petición `POST /api/v1/authentication/sign-in` y el token JWT devuelto, que la aplicación envía en el encabezado `Authorization` de las siguientes peticiones.

![Cierre de sesión](assets/img/sprint3/exec-04-sign-out.png)

**US43.** Opción de cierre de sesión en el menú del usuario, que elimina el token y redirige al inicio de sesión.

<h4>Arrendatario</h4>

![Búsqueda desde los Web Services](assets/img/sprint3/exec-05-vehicle-search.png)

**TS27 y TS28.** Búsqueda de vehículos cercanos con filtros, con los resultados obtenidos de los Web Services.

![Reserva persistida](assets/img/sprint3/exec-06-booking.png)

**TS31.** Creación de una reserva. La solicitud queda registrada en la base de datos con estado `pending`.

![Favoritos y mensajes](assets/img/sprint3/exec-07-favorites-messages.png)

**TS51 y TS52.** Vehículos favoritos y mensajería con el propietario, almacenados en los Web Services.

<h4>Propietario</h4>

![Solicitud confirmada](assets/img/sprint3/exec-08-owner-confirm.png)

**TS31 y TS53.** El propietario confirma la solicitud y el arrendatario recibe la notificación correspondiente.

![Gestión de flota](assets/img/sprint3/exec-09-fleet.png)

**TS29 y TS30.** Publicación de un vehículo y bloqueo de fechas en el calendario de disponibilidad.

![Métricas y reseñas](assets/img/sprint3/exec-10-owner-dashboard.png)

**TS32 y TS33.** Inicio del propietario con métricas calculadas por los Web Services y calificaciones recibidas.

![Perfil](assets/img/sprint3/exec-11-profile.png)

**TS54.** Edición del perfil y cambio de contraseña.


#### 5.2.3.6. Services Documentation Evidence for Sprint Review.

En este Sprint se implementó y documentó con OpenAPI (Swagger) la primera versión de los RESTful Web Services de Veygo, desarrollados con ASP.NET Core y Entity Framework Core. Los endpoints se organizan por bounded context, utilizan el prefijo `/api/v1` y reemplazan los recursos de la Fake API del Sprint 2. Todos los endpoints, salvo el registro y el inicio de sesión, requieren un token JWT en el encabezado `Authorization: Bearer {token}`. Los mensajes de la API se devuelven en inglés por defecto y en español latinoamericano cuando la petición incluye el encabezado `Accept-Language: es-419`. Los errores se devuelven en el formato estándar `ProblemDetails`.

Documentación desplegada (Swagger UI): https://<url-de-los-web-services>/swagger

Repositorio de los Web Services: https://github.com/1ASI0729-2620-4399-G3-Veygo/backend

| Bounded Context | Endpoint | Acción | Sintaxis de llamada | Parámetros | Descripción del response |
|---|---|---|---|---|---|
| IAM | `/api/v1/authentication/sign-up` | POST | `POST /api/v1/authentication/sign-up` | Body: `firstName`, `lastName`, `email`, `password`, `role` (`renter` u `owner`) | `201 Created` con el usuario registrado, sin la contraseña. `409 Conflict` si el correo ya existe. |
| IAM | `/api/v1/authentication/sign-in` | POST | `POST /api/v1/authentication/sign-in` | Body: `email`, `password` | `200 OK` con el id, el rol y el token JWT del usuario. `401 Unauthorized` si las credenciales son incorrectas. |
| IAM | `/api/v1/users/{id}` | GET, PUT, DELETE | `GET /api/v1/users/{id}` <br> `PUT /api/v1/users/{id}` <br> `DELETE /api/v1/users/{id}` | Path: `id`. Body (PUT): datos personales, licencia y preferencias | Perfil del usuario, perfil actualizado o `204 No Content` al eliminar la cuenta. |
| IAM | `/api/v1/users/{id}/password` | PATCH | `PATCH /api/v1/users/{id}/password` | Path: `id`. Body: `currentPassword`, `newPassword` | `204 No Content`. `400 Bad Request` si la contraseña actual no coincide. |
| Fleet | `/api/v1/vehicles` | GET, POST | `GET /api/v1/vehicles?latitude={lat}&longitude={lng}&radiusKm={km}&startDate={fecha}&endDate={fecha}&type={tipo}&transmission={tipo}&fuelType={tipo}&minPrice={n}&maxPrice={n}&minRating={n}` <br> `GET /api/v1/vehicles?ownerId={id}` <br> `POST /api/v1/vehicles` | Query: ubicación, radio, fechas y filtros (todos opcionales), `ownerId`. Body (POST): datos del vehículo | Lista de vehículos publicados que cumplen los filtros, ordenados por distancia, o vehículo creado con `201 Created`. |
| Fleet | `/api/v1/vehicles/{id}` | GET, PUT, PATCH, DELETE | `GET /api/v1/vehicles/{id}` <br> `PUT /api/v1/vehicles/{id}` <br> `PATCH /api/v1/vehicles/{id}/publication` <br> `DELETE /api/v1/vehicles/{id}` | Path: `id`. Body (PATCH): `published` | Detalle, vehículo actualizado, estado de publicación o `204 No Content`. |
| Fleet | `/api/v1/vehicles/{vehicleId}/blocked-dates` | GET, POST, DELETE | `GET /api/v1/vehicles/{vehicleId}/blocked-dates` <br> `POST /api/v1/vehicles/{vehicleId}/blocked-dates` <br> `DELETE /api/v1/vehicles/{vehicleId}/blocked-dates/{id}` | Path: `vehicleId`, `id`. Body (POST): `startDate`, `endDate` | Fechas bloqueadas del vehículo. `409 Conflict` si el bloqueo se cruza con una reserva confirmada. |
| Booking | `/api/v1/bookings` | GET, POST | `GET /api/v1/bookings?renterId={id}` <br> `GET /api/v1/bookings?ownerId={id}&status={estado}` <br> `GET /api/v1/bookings?vehicleId={id}` <br> `POST /api/v1/bookings` | Query: `renterId`, `ownerId`, `vehicleId`, `status`. Body (POST): `vehicleId`, `startDate`, `endDate`, `paymentMethod` | Lista de reservas o reserva creada en estado `pending`. `409 Conflict` si las fechas no están disponibles. |
| Booking | `/api/v1/bookings/{id}` | GET, PATCH | `GET /api/v1/bookings/{id}` <br> `PATCH /api/v1/bookings/{id}/confirm` <br> `PATCH /api/v1/bookings/{id}/reject` <br> `PATCH /api/v1/bookings/{id}/cancel` <br> `PATCH /api/v1/bookings/{id}/complete` | Path: `id` | Reserva con su nuevo estado. `400 Bad Request` si la transición no es válida, por ejemplo al confirmar una reserva cancelada. |
| Engagement | `/api/v1/favorites` | GET, POST, DELETE | `GET /api/v1/favorites?renterId={id}` <br> `POST /api/v1/favorites` <br> `DELETE /api/v1/favorites/{id}` | Query: `renterId`. Body (POST): `renterId`, `vehicleId` | Vehículos favoritos del arrendatario, favorito creado o `204 No Content`. |
| Communication | `/api/v1/conversations` | GET, POST | `GET /api/v1/conversations?userId={id}` <br> `POST /api/v1/conversations` | Query: `userId`. Body (POST): `renterId`, `ownerId`, `vehicleId` | Conversaciones del usuario ordenadas por último mensaje, o conversación creada. |
| Communication | `/api/v1/conversations/{id}/messages` | GET, POST | `GET /api/v1/conversations/{id}/messages` <br> `POST /api/v1/conversations/{id}/messages` <br> `PATCH /api/v1/messages/{id}/read` | Path: `id`. Body (POST): `content` | Mensajes de la conversación, mensaje enviado o `204 No Content` al marcarlo como leído. |
| Notification | `/api/v1/notifications` | GET, PATCH | `GET /api/v1/notifications?userId={id}` <br> `PATCH /api/v1/notifications/{id}/read` | Query: `userId`. Path: `id` | Últimas notificaciones del usuario o `204 No Content` al marcarla como leída. |
| Reputation | `/api/v1/reviews` | GET, POST | `GET /api/v1/reviews?vehicleId={id}` <br> `GET /api/v1/reviews?ownerId={id}` <br> `POST /api/v1/reviews` | Query: `vehicleId`, `ownerId`. Body (POST): `bookingId`, `rating`, `comment` | Reseñas o reseña creada. `409 Conflict` si la reserva ya tiene reseña y `400 Bad Request` si no está finalizada. |
| Reputation | `/api/v1/owners/{ownerId}/reputation` | GET | `GET /api/v1/owners/{ownerId}/reputation` | Path: `ownerId` | Promedio, cantidad de reseñas, distribución de estrellas y nivel de reputación. |
| Dashboard | `/api/v1/owners/{ownerId}/metrics` | GET | `GET /api/v1/owners/{ownerId}/metrics` | Path: `ownerId` | Vehículos activos, reservas próximas, ingresos del mes y calificación promedio. |
| Dashboard | `/api/v1/owners/{ownerId}/transactions` | GET | `GET /api/v1/owners/{ownerId}/transactions?from={fecha}&to={fecha}` | Path: `ownerId`. Query: `from`, `to` | Transacciones del rango de fechas, con el total por mes y por vehículo. |

Ejemplo de petición y respuesta de `POST /api/v1/authentication/sign-in`:

```json
{
  "email": "leo.ramos@veygo.pe",
  "password": "Veygo2026!"
}
```

```json
{
  "id": 1,
  "email": "leo.ramos@veygo.pe",
  "role": "renter",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

La respuesta devuelve los datos básicos del usuario autenticado y el token JWT, que el Frontend Web Application almacena y envía en las siguientes peticiones.

Ejemplo de petición y respuesta de `POST /api/v1/bookings`:

```json
{
  "vehicleId": 1,
  "startDate": "2026-11-20",
  "endDate": "2026-11-23",
  "paymentMethod": "card"
}
```

```json
{
  "id": 16,
  "vehicleId": 1,
  "renterId": 1,
  "ownerId": 2,
  "startDate": "2026-11-20",
  "endDate": "2026-11-23",
  "pricePerDay": 180,
  "totalPrice": 540,
  "status": "pending",
  "paymentMethod": "card",
  "createdAt": "2026-11-05T15:30:00Z"
}
```

El arrendatario se obtiene del token, por lo que no se envía en la petición. Los Web Services validan que las fechas no se crucen con reservas confirmadas ni con fechas bloqueadas, calculan el total y registran la reserva en estado `pending`.

Ejemplo de error de `POST /api/v1/bookings` con `Accept-Language: es-419`:

```json
{
  "title": "Conflict",
  "status": 409,
  "detail": "El vehículo no está disponible en las fechas seleccionadas."
}
```

<h4>Interacción con la documentación</h4>

![Swagger UI](assets/img/sprint3/swagger-01-overview.png)

Vista general de Swagger UI con los endpoints agrupados por bounded context.

![Autenticación en Swagger](assets/img/sprint3/swagger-02-sign-in.png)

Ejecución de `POST /api/v1/authentication/sign-in` con la cuenta de prueba. El token obtenido se registra con el botón **Authorize** para probar los endpoints protegidos.

![Creación de reserva en Swagger](assets/img/sprint3/swagger-03-create-booking.png)

Ejecución de `POST /api/v1/bookings` con datos de muestra y respuesta `201 Created`.

![Confirmación de reserva en Swagger](assets/img/sprint3/swagger-04-confirm-booking.png)

Ejecución de `PATCH /api/v1/bookings/{id}/confirm` con la cuenta del propietario. La reserva cambia a estado `confirmed`.

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed by | Committed on (Date) |
|---|---|---|---|---|---|---|
| (se completa con los commits reales de documentación) | | | | | | |


#### 5.2.3.7. Software Deployment Evidence for Sprint Review.

En este Sprint se desplegaron tres productos: la primera versión de los **Web Services** en Render, con su base de datos MySQL en Aiven; una nueva versión del **Frontend Web Application** en Firebase Hosting, conectada a los Web Services; y una nueva versión de la **Landing Page** en GitHub Pages. Con este despliegue, la Fake API del Sprint 2 dejó de ser utilizada por la aplicación.

| Producto | Plataforma | Versión | URL |
|---|---|---|---|
| Landing Page | GitHub Pages | v1.1.0 | https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/ |
| Frontend Web Application | Firebase Hosting | v1.1.0 | https://veygo-web-app.web.app |
| Web Services (RESTful API) | Render | v1.0.0 | https://<url-de-los-web-services>/swagger |
| Base de datos MySQL | Aiven | — | (acceso privado) |

<h4>Base de datos MySQL en Aiven</h4>

1. Se creó una cuenta en Aiven y un servicio **MySQL** en el plan gratuito.

![Aiven crear servicio](assets/img/sprint3/deploy-01-aiven-create-mysql.png)

2. Una vez activo el servicio, se obtuvieron los datos de conexión (host, puerto, usuario y base de datos). Estos datos se registraron como variables de entorno en Render y no se incluyeron en el repositorio.

![Aiven servicio activo](assets/img/sprint3/deploy-02-aiven-running.png)

<h4>Despliegue de los Web Services en Render</h4>

3. Se agregó al repositorio `backend` un `Dockerfile` multi-stage, que compila el proyecto con la imagen del SDK de .NET y lo ejecuta con la imagen de ASP.NET Core runtime.

![Dockerfile](assets/img/sprint3/deploy-03-dockerfile.png)

4. En Render se creó un nuevo **Web Service** a partir del repositorio `backend`, con la rama `main` y el entorno **Docker**.

![Render nuevo servicio](assets/img/sprint3/deploy-04-render-backend-new.png)

5. Se configuraron las variables de entorno: la cadena de conexión a MySQL (`ConnectionStrings__DefaultConnection`), la clave para firmar los tokens JWT (`TokenSettings__Secret`), el entorno (`ASPNETCORE_ENVIRONMENT=Production`) y los orígenes permitidos por CORS, que incluyen el dominio de Firebase Hosting.

![Render variables de entorno](assets/img/sprint3/deploy-05-render-env-vars.png)

6. Al iniciar, los Web Services crearon las tablas en la base de datos mediante Entity Framework Core. El despliegue terminó correctamente y la documentación quedó disponible en Swagger UI.

![Render desplegado](assets/img/sprint3/deploy-06-render-backend-live.png)

![Swagger desplegado](assets/img/sprint3/deploy-07-swagger-live.png)

<h4>Nueva versión del Frontend Web Application en Firebase Hosting</h4>

7. Se actualizó `.env.production` para que la variable de la URL base de la API apunte a los Web Services desplegados en Render, en lugar de la Fake API.

![Variables de producción](assets/img/sprint3/deploy-08-env-production.png)

8. Se generó la versión de producción con `npm run build` y se desplegó con `firebase deploy --only hosting`.

![Firebase deploy](assets/img/sprint3/deploy-09-firebase-deploy.png)

<h4>Nueva versión de la Landing Page en GitHub Pages</h4>

9. Se integraron a `main` los cambios de la Landing Page (preguntas frecuentes, suscripción, atributos ARIA, textos en es-419 y el Video About-the-Product incrustado). GitHub Pages publicó automáticamente la nueva versión mediante el flujo `pages-build-deployment`.

![GitHub Actions Landing Page](assets/img/sprint3/deploy-10-pages-actions.png)

10. Se crearon los tags de versión de cada producto según Semantic Versioning: `v1.0.0` en `backend` y `v1.1.0` en `frontend` y `landing-Page`.

![Releases](assets/img/sprint3/deploy-11-tags.png)


#### 5.2.3.8. Team Collaboration Insights during Sprint.

Durante este Sprint el equipo trabajó en los tres repositorios de la organización 1ASI0729-2620-4399-G3-Veygo aplicando GitFlow: `backend` para los Web Services, `frontend` para el Frontend Web Application y `landing-Page` para la Landing Page. Cada integrante desarrolló su bounded context de los Web Services en una rama `feature/*`, lo integró en el frontend y realizó una tarea en la Landing Page. Cada aporte se integró a `develop` mediante un Pull Request revisado por al menos otro integrante, y finalmente `develop` se integró a `main` para el despliegue.

A diferencia del Sprint 2, la carga de trabajo se distribuyó de forma equilibrada: todos los integrantes participaron en la implementación de los tres productos, como se resume en la siguiente tabla.

| Integrante | Web Services (`backend`) | Frontend Web Application (`frontend`) | Landing Page (`landing-Page`) | Total de commits |
|---|---|---|---|---|
| Flores Apaico, Josué Antonio | feature/shared-kernel, feature/iam — _n_ commits | feature/iam-integration — _n_ commits | feature/navigation-a11y — _n_ commits | _n_ |
| Flores Siguas, Marlon Alessandro | feature/fleet — _n_ commits | feature/fleet-integration — _n_ commits | feature/catalog-a11y — _n_ commits | _n_ |
| Su Caletti, Eddo | feature/booking — _n_ commits | feature/booking-integration — _n_ commits | feature/search-a11y — _n_ commits | _n_ |
| Cano Ortiz, Fabrizio Hamet | feature/communication, feature/notification, feature/engagement, feature/profile — _n_ commits | feature/communication-integration — _n_ commits | feature/trust-a11y — _n_ commits | _n_ |
| Ibañez Torres, Ivonne Beatriz | feature/reputation, feature/dashboard — _n_ commits | feature/dashboard-integration — _n_ commits | feature/faq, feature/subscription — _n_ commits | _n_ |
| | | | **Total** | **_n_** |

| Repositorio | Pull Requests integrados | Commits de desarrollo | Commits de merge | Tag de versión |
|---|---|---|---|---|
| backend | _n_ | _n_ | _n_ | v1.0.0 |
| frontend | _n_ | _n_ | _n_ | v1.1.0 |
| landing-Page | _n_ | _n_ | _n_ | v1.1.0 |

A continuación, se presentan las capturas de los analíticos de GitHub que evidencian la participación de los miembros del equipo en cada repositorio durante este Sprint:

<h4>Web Services</h4>

![Contributors backend](assets/img/sprint3/insights-backend-contributors.png)

Contribuciones por integrante en el repositorio `backend`.

![Network backend](assets/img/sprint3/insights-backend-network.png)

Gráfico de red con las ramas `feature/*` de los bounded contexts integradas a `develop` y `main`.

<h4>Frontend Web Application</h4>

![Contributors frontend](assets/img/sprint3/insights-frontend-contributors.png)

Contribuciones por integrante en el repositorio `frontend` durante el Sprint 3.

<h4>Landing Page</h4>

![Contributors landing](assets/img/sprint3/insights-landing-contributors.png)

Contribuciones por integrante en el repositorio `landing-Page`.

## 5.3. Validation Interviews.

En esta sección se registran las entrevistas de validación realizadas al término del Sprint 3, en las que usuarios de los dos segmentos objetivo de Veygo interactuaron con la Landing Page y con el Frontend Web Application desplegados. El objetivo fue comprobar si los productos permiten completar las tareas principales de cada segmento de forma sencilla, identificar problemas de usabilidad, arquitectura de información y diseño inclusivo, y contrastar los resultados con los supuestos e hipótesis planteados en el proceso de Lean UX.

### 5.3.1. Diseño de Entrevistas.

Las sesiones de validación se realizaron de forma virtual mediante Google Meet. El entrevistado compartió su pantalla mientras utilizaba los productos desplegados, y la sesión se grabó con su consentimiento. Cada sesión duró entre 15 y 20 minutos y siguió la técnica de pensamiento en voz alta (think aloud): el entrevistado comentó lo que veía, esperaba y le resultaba confuso mientras realizaba cada tarea, y el entrevistador solo intervino cuando el participante no pudo continuar.

**Perfil de los participantes**

| Segmento | Perfil | Cantidad |
|---|---|---|
| Segmento 1: Clientes / Arrendatarios | Personas de 18 a 40 años que viven en Lima, que han alquilado un vehículo o consideran hacerlo para viajes, trabajo o trámites, y que no cuentan con un vehículo propio disponible. | 3 a 5 |
| Segmento 2: Propietarios particulares / Arrendadores | Personas que viven en Lima, que tienen un auto o una moto que no utilizan todos los días y que han alquilado su vehículo o les interesa generar ingresos con él. | 3 a 5 |

**Estructura de la sesión**

| Parte | Duración | Contenido |
|---|---|---|
| 1. Introducción | 2 min | Presentación del entrevistador, explicación del objetivo de la sesión, solicitud de consentimiento para grabar y datos del entrevistado (nombre, edad, distrito y ocupación). |
| 2. Landing Page | 4 min | Tareas en la Landing Page, sin explicación previa del producto. |
| 3. Web Application | 10 min | Tareas en la aplicación según el segmento, utilizando una cuenta de prueba. |
| 4. Cierre | 3 min | Preguntas de cierre sobre la experiencia general. |

**User flows evaluados en la Landing Page (ambos segmentos)**

| # | Tarea | Qué se observa |
|---|---|---|
| L1 | Explicar con sus palabras qué ofrece Veygo después de recorrer la página durante un minuto. | Claridad de la propuesta de valor. |
| L2 | Cambiar el idioma de la página a español o a inglés. | Visibilidad del selector de idioma. |
| L3 | Encontrar la respuesta a una duda en la sección de preguntas frecuentes. | Organización y búsqueda de información. |
| L4 | Registrarse como arrendatario o como propietario desde la Landing Page. | Claridad de la redirección según el rol. |

**User flows evaluados en la Web Application: Segmento 1 (Arrendatarios)**

| # | Tarea | User Stories relacionadas |
|---|---|---|
| A1 | Crear una cuenta como arrendatario e iniciar sesión. | US37, US02 |
| A2 | Buscar un vehículo automático o eléctrico disponible cerca de su distrito para el próximo fin de semana. | US03, US04 |
| A3 | Revisar el detalle de un vehículo y solicitar su reserva. | US38, US17 |
| A4 | Guardar un vehículo como favorito y enviar un mensaje al propietario. | US39, US41 |
| A5 | Revisar el estado de su reserva y cancelarla. | US20, US19 |

**User flows evaluados en la Web Application: Segmento 2 (Propietarios)**

| # | Tarea | User Stories relacionadas |
|---|---|---|
| P1 | Crear una cuenta como propietario e iniciar sesión. | US37, US02 |
| P2 | Publicar un vehículo con fotos, especificaciones y precio por día. | US15 |
| P3 | Bloquear en el calendario los días en que no podrá alquilar el vehículo. | US05 |
| P4 | Aceptar o rechazar una solicitud de reserva pendiente. | US18, US21 |
| P5 | Revisar sus ingresos del mes y las calificaciones recibidas. | US06, US42, US07 |

**Preguntas después de cada tarea**

- En una escala del 1 (muy difícil) al 7 (muy fácil), ¿qué tan fácil fue realizar esta tarea?
- ¿Hubo algo que no esperabas o que te confundió?

**Preguntas de cierre**

1. ¿Qué fue lo que más te gustó de Veygo y qué fue lo que menos te gustó?
2. ¿Confiarías en Veygo para alquilar un vehículo a un desconocido (o para alquilar el vehículo de un desconocido)? ¿Por qué?
3. ¿Qué información o función te faltó para sentirte seguro durante el proceso?
4. ¿Qué tan probable es que recomiendes Veygo a un amigo, del 0 al 10?
5. ¿Hay algo más que quieras comentar sobre la experiencia?

**Indicadores registrados por tarea:** tarea completada sin ayuda, completada con ayuda o no completada; tiempo aproximado; errores cometidos; y calificación de facilidad del 1 al 7.

### 5.3.2. Registro de Entrevistas.

A continuación, se registran las entrevistas de validación realizadas con cada segmento objetivo. Todas las sesiones se consolidaron en un solo video.

Video de las entrevistas de validación: <URL del video en Microsoft Stream>

![Video de entrevistas de validación](assets/img/sprint3/validation-video.png)

#### Segmento 1: Clientes / Arrendatarios

##### Entrevista 1

| Campo | Detalle |
|---|---|
| **Nombres** | |
| **Apellidos** | |
| **Edad** | |
| **Distrito** | |
| **Ocupación** | |
| **Fecha de la entrevista** | |
| **Entrevistador** | |
| **Inicio en el video** | 00:00 |
| **Duración** | 00:00 |

![Entrevista 1](assets/img/sprint3/validation-01.png)

**Resumen:** (Redactar las principales apreciaciones del entrevistado sobre cada tarea: qué tareas completó con facilidad, dónde dudó o se equivocó, qué le gustó y qué le faltó, y sus respuestas más relevantes a las preguntas de cierre.)

| Tarea | Resultado | Facilidad (1-7) | Observación principal |
|---|---|---|---|
| L1 | | | |
| L2 | | | |
| L3 | | | |
| L4 | | | |
| A1 | | | |
| A2 | | | |
| A3 | | | |
| A4 | | | |
| A5 | | | |

(Repetir la estructura de la Entrevista 1 para las Entrevistas 2 y 3 del Segmento 1.)

#### Segmento 2: Propietarios particulares / Arrendadores

##### Entrevista 4

| Campo | Detalle |
|---|---|
| **Nombres** | |
| **Apellidos** | |
| **Edad** | |
| **Distrito** | |
| **Ocupación** | |
| **Vehículo que posee** | |
| **Fecha de la entrevista** | |
| **Entrevistador** | |
| **Inicio en el video** | 00:00 |
| **Duración** | 00:00 |

![Entrevista 4](assets/img/sprint3/validation-04.png)

**Resumen:** (Redactar las principales apreciaciones del entrevistado sobre cada tarea.)

| Tarea | Resultado | Facilidad (1-7) | Observación principal |
|---|---|---|---|
| L1 | | | |
| L2 | | | |
| L3 | | | |
| L4 | | | |
| P1 | | | |
| P2 | | | |
| P3 | | | |
| P4 | | | |
| P5 | | | |

(Repetir la estructura de la Entrevista 4 para las Entrevistas 5 y 6 del Segmento 2.)

#### Resultados generales

| Tarea | Completada sin ayuda | Completada con ayuda | No completada | Facilidad promedio (1-7) |
|---|---|---|---|---|
| L1 | | | | |
| L2 | | | | |
| L3 | | | | |
| L4 | | | | |
| A1 / P1 | | | | |
| A2 | | | | |
| A3 | | | | |
| A4 | | | | |
| A5 | | | | |
| P2 | | | | |
| P3 | | | | |
| P4 | | | | |
| P5 | | | | |

(Redactar un párrafo con el análisis general: tareas más fáciles y más difíciles, problemas que se repitieron entre entrevistados y diferencias entre segmentos.)

### 5.3.3. Evaluaciones según heurísticas.

**UX Heuristics & Principles Evaluation**
**Usability – Inclusive Design – Information Architecture**

| Campo | Detalle |
|---|---|
| **CARRERA** | Ingeniería de Software |
| **CURSO** | Aplicaciones Web |
| **SECCIÓN** | <código de la sección> |
| **PROFESORES** | <nombre del profesor> |
| **AUDITOR** | Zyntra |
| **CLIENTE(S)** | <nombres de los entrevistados> |

**SITE o APP A EVALUAR:**

Veygo: Landing Page (https://1asi0729-2620-4399-g3-veygo.github.io/landing-Page/) y Frontend Web Application (https://veygo-web-app.web.app).

**TAREAS A EVALUAR:**

El alcance de esta evaluación incluye la revisión de la usabilidad de las siguientes tareas:

1. Comprensión de la propuesta de valor en la Landing Page.
2. Cambio de idioma de la Landing Page y de la aplicación.
3. Consulta de las preguntas frecuentes.
4. Registro de un usuario nuevo según su rol e inicio de sesión.
5. Búsqueda de vehículos cercanos con filtros.
6. Consulta del detalle de un vehículo y solicitud de reserva.
7. Registro de vehículos favoritos y envío de mensajes al propietario.
8. Consulta y cancelación de una reserva.
9. Publicación de un vehículo.
10. Bloqueo de fechas en el calendario de disponibilidad.
11. Aceptación o rechazo de una solicitud de reserva.
12. Consulta de ingresos, transacciones y calificaciones del propietario.

No están incluidas en esta versión de la evaluación las siguientes tareas:

1. Verificación de identidad con DNI y licencia de conducir.
2. Pago de la reserva y reembolso por cancelación.
3. Registro de la entrega y devolución del vehículo.
4. Recuperación de contraseña.

**ESCALA DE SEVERIDAD:**

Los errores serán puntuados tomando en cuenta la siguiente escala de severidad:

| Nivel | Descripción |
|---|---|
| 1 | Problema superficial: puede ser fácilmente superado por el usuario u ocurre con muy poca frecuencia. No necesita ser arreglado a no ser que exista disponibilidad de tiempo. |
| 2 | Problema menor: puede ocurrir un poco más frecuentemente o es un poco más difícil de superar para el usuario. Se le debería asignar una prioridad baja resolverlo de cara al siguiente release. |
| 3 | Problema mayor: ocurre frecuentemente o los usuarios no son capaces de resolverlo. Es importante que sea corregido y se le debe asignar una prioridad alta. |
| 4 | Problema muy grave: un error de gran impacto que impide al usuario continuar con el uso de la herramienta. Es imperativo que sea corregido antes del lanzamiento. |

**TABLA RESUMEN:**

| # | Problema | Escala de severidad | Heurística/Principio violada(o) |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
| 4 | | | |
| 5 | | | |

**DESCRIPCIÓN DE PROBLEMAS:**

**PROBLEMA #1:** <título del problema>

**Severidad:** <1 a 4>

**Heurística violada:** <Usability / Inclusive Design / Information Architecture: nombre de la heurística o principio>

**Problema:** <descripción de lo que ocurrió, en qué pantalla y qué entrevistados lo experimentaron>

![Problema 1](assets/img/sprint3/heuristic-01.png)

**Recomendación:** <cambio propuesto para resolverlo>

(Repetir la estructura para cada problema de la tabla resumen.)

## 5.4. Video About-the-Product.

El Video About-the-Product está dirigido a los visitantes de la Landing Page que desean conocer el modelo de negocio de Veygo y a los usuarios de la aplicación que quieren saber cómo realizar sus tareas principales. Con un tono cercano y confiable, el video presenta el problema de alquilar vehículos entre particulares por canales informales, la propuesta de Veygo para arrendatarios y propietarios, y una demostración de los flujos principales de la aplicación. Además, incluye testimonios de usuarios de ambos segmentos que participaron en las entrevistas de validación.

| Tiempo | Sección | Contenido |
|---|---|---|
| 00:00 | Problema | Situaciones de arrendatarios y propietarios que alquilan vehículos por redes sociales o contactos, con desconfianza y coordinación informal. |
| 00:20 | Propuesta de valor | Presentación de Veygo como marketplace seguro de alquiler de vehículos entre particulares en Lima. |
| 00:35 | Arrendatario | Demostración de la búsqueda en el mapa, los filtros, el detalle del vehículo y la solicitud de reserva. |
| 01:05 | Propietario | Demostración de la publicación de un vehículo, el calendario de disponibilidad, la confirmación de la reserva y las métricas. |
| 01:35 | Confianza | Reseñas, reputación, notificaciones y mensajería dentro de la plataforma. |
| 01:50 | Testimonios | Opinión de un arrendatario y de un propietario entrevistados en la validación. |
| 02:20 | Cierre | Llamada a la acción para registrarse en Veygo y enlace a la plataforma. |

![Video About-the-Product](assets/img/sprint3/about-the-product.png)

Duración: 00:00

Video en Microsoft Stream: <URL>

Video en YouTube (incrustado en la Landing Page): <URL>

