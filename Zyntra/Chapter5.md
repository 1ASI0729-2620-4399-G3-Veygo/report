# Capítulo V: Product Implementation, Validation & Deployment.

---

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

Landing Page:
Acceptance Test (.feature):


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

En esta sección se detallan las convenciones de estilo y las estructuras empleadas en el desarrollo del sitio web, abarcando los lenguajes HTML, CSS y Gherkin. Estas normas fueron adoptadas con el propósito de mantener un código limpio, organizado y fácilmente mantenible por todos los integrantes del equipo.

<!--Aca tenemos que poner ciertas caracteristicas del codigo que tengamos de la landing y test -ivn -->

### 5.1.4. Software Deployment Configuration. 

En esta sección, daremos el paso a paso para realizar el deploy de nuestra página dentro de github.

<h4>Deploy con GitHub Pages: </h4>

<!-- Aca solo es la descripción de como deployamos la landingpage con githubpages-->

---

## 5.2. Landing Page, Services & Applications Implementation. 

### 5.2.1. Sprint 1

En esta parte, registramos y explicaremos el avance en términos de producto y trabajo colaborativo. Incluye tres secciones internas: Sprint Backlog 1, User Interface & Execution y Team Collaboration Insights.

#### 5.2.1.1. Sprint Planning 1

Para este primer Sprint, el equipo estableció como objetivo principal la implementación y despliegue de la primera versión de la Landing Page del sistema Zyntra.

<!--Aca va el cuadro de la sprint 1, que basicamente solo es como un resumen de la reunion que debemos tener, detallando detalles como el organizador, fecha, hora, esas cosas -->

#### 5.2.1.2. Aspect Leaders and Collaborators

<!-- Aca va lo que hizo cada quien-->

#### 5.2.1.3. Sprint Backlog 1

El objetivo principal de este Sprint fue implementar y desplegar la primera versión de la Landing Page del sistema Zyntra.

#### 5.2.1.4. Development Evidence for Sprint Review. 

<!-- foto de colaboración en github-->

#### 5.2.1.5. Execution Evidence for Sprint Review

Al término del Sprint 1, el equipo logró implementar y desplegar satisfactoriamente la primera versión de la Landing Page del sistema Zyntra. La página se encuentra disponible públicamente mediante GitHub Pages.

<!-- Aca tendremos que detallar las caracteristicas de la landingpage, como el hero, los apartados, el footer -ivn -->

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

Durante el Sprint 1, el alcance de implementación se limitó exclusivamente al Landing Page estático. No se desarrollaron ni desplegaron Web Services (RESTful API) en esta iteración, por lo que no aplica documentación de endpoints para este Sprint. La documentación de servicios web se incorporará a partir del Sprint 2, conforme a lo planificado en el Product Backlog.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

<!--Descripción hhhh y despliegue como su nombre lo dice kkkkkkk  -->


#### 5.2.1.8. Team Collaboration Insights during Sprint

<!-- captura del commits over time del github de la landing page-->