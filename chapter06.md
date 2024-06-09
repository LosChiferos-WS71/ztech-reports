# Capítulo VI: Product Implementation, Validation & Deployment

## 6.1. Software Configuration Management

### 6.1.1. Software Development Environment Configuration

Este apartado detalla los productos de software necesarios para colaborar en el ciclo de vida de los productos digitales en el proyecto de IoT. Incluye nombres de productos, su propósito en el proyecto y las rutas de referencia/descarga para acceder a ellos.

**Visual Studio Code**

> Este editor de código será utilizado para desarrollar la landing page y las aplicaciones web y móviles. Angular se empleará para el desarrollo web, mientras que Flutter se utilizará para las aplicaciones móviles.

Link: https://code.visualstudio.com/download

**Wokwi**

> Se implementará para desarrollar nuestra solución IoT y embedded application.

Link: https://wokwi.com/

**Github**

> Esta plataforma será utilizada para gestionar el control de versiones de todos nuestros repositorios.

Link: https://github.com/

**Figma**

> Esta herramienta se emplea para la creación de prototipos de nuestras aplicaciones web y móviles.

Link: https://www.figma.com/

**Netlify**

> Contribuirá al despliegue de las aplicaciones frontend.

Link: https://www.netlify.com/

**Railway**

> Será utilizado para desplegar el servicio backend.

Link: https://railway.app/

**Miro**

> Se utiliza para realizar sesiones de lluvia de ideas y para secciones específicas del informe, como el escenario actual y el escenario deseado.

Link: https://miro.com/es/

**Uxpressia**

> Se emplea para representar las secciones de Needfinding.

Link: https://uxpressia.com/

**Lucidchart**

> Se utiliza para la creación de diagramas de clases y diagramas de bases de datos.

Link: https://www.lucidchart.com/pages

**Visual Paradigm**

> Se emplea para diagramar la arquitectura de software de nuestro proyecto.

Link: https://www.visual-paradigm.com/

### 6.1.2. Source Code Management

**Landing Page**

![](./assets/6.1.2.SourceCodeManagement/landing_page_github.png)

Link: https://github.com/LosChiferos-WS71/ztech-landing-page

**Web Services**

![](./assets/6.1.2.SourceCodeManagement/web_services_github.png)

Link: https://github.com/LosChiferos-WS71/ztech-web-service

**Frontend Web Application**

![](./assets/6.1.2.SourceCodeManagement/frontend_web_github.png)

Link: https://github.com/LosChiferos-WS71/ztech-web-application

**Frontend Mobile Application**

![](./assets/6.1.2.SourceCodeManagement/frontend_mobile_github.png)

Link: https://github.com/LosChiferos-WS71/ztech-mobile-application

----

**Convenciones de GitHub**

The main branch:

El modelo de desarrollo se basa en prácticas establecidas. El repositorio central contiene dos ramas principales con una vida útil indefinida:

master: Esta rama es conocida por todos los usuarios de Git. Representa un estado listo para producción.
develop: Paralelamente a la rama master, la rama develop alberga los cambios de desarrollo más recientes para la próxima versión. Actúa como la rama de integración y es donde se generan las compilaciones automáticas nocturnas.
Cuando el código en la rama develop se estabiliza y está listo para ser lanzado, todos los cambios se fusionan de nuevo en master y se etiquetan con un número de versión. Esto asegura que cada fusión en master constituya un nuevo lanzamiento de producción, facilitando la automatización potencial de la implementación de software.

![](./assets/6.1.2.SourceCodeManagement/main-branches@2x.png)

Feature branches:

Bifurcadas Desde: develop
Fusionadas De Nuevo En: develop
Convención de Nombres: Cualquier cosa excepto master, develop, release-, o hotfix-
Las ramas de características, también conocidas como ramas de temas, se crean para desarrollar nuevas características para lanzamientos futuros próximos o distantes. Estas ramas persisten hasta que la característica esté lista para ser incorporada en la rama develop o sea descartada si se considera inadecuada.

![](./assets/6.1.2.SourceCodeManagement/fb@2x.png)

### 6.1.3. Source Code Style Guide & Conventions

Como convención general, todo el código realizado por los miembros del equipo debe redactarse en
completo inglés.

**HTML**

Use Lowercase Element Names: Se recomienda usar lowercase para los nombres de los elementos HTML.

Close All HTML Elements: Se recomienda cerrar todos los elementos HTML.

Use Lowercase Attribute Names: Se recomienda usar lowercase para los nombres de los atributos HTML.

Always Specify alt, width, and height for Images: Se recomienda seguir estas convenciones en caso de que la imagen no se puede mostrar y ayudar con la accesibilidad del contenido.

Spaces and Equal Signs: Se recomienda no usar espacios en blanco entre las entidades para una mejor lectura.

Para más información sobre las convenciones de HTML se usará como referencia:
https://www.w3schools.com/html/html5_syntax.asp

**CSS**

ID and Class Naming: Usar nombres de clases e ID significativos que expresen el propósito del elemento.

ID and Class Name Style: Usar nombres cortos para nombrar ID o clases, pero lo suficientemente largo para saber cuál es su
propósito.

Shorthand Properties: Usar CSS shothand properties tanto como sea posible para que el código sea más eficiente y entendible.

ID and Class Name Delimiters: Separar las palabras en ID y clases con un guión.

Selector and Declaration Separation: Separar los selectores y declaraciones en nuevas líneas.

Para más información sobre las convenciones de CSS se usará como referencia:
https://google.github.io/styleguide/htmlcssguide.html#CSS

**JavaScript**

Use expanded syntax: Cada línea de JavaScript en una nueva línea, con la llave de apertura en la misma línea de su
declaración y la llave de cierre en una nueva línea al final.

Variable naming: Para el nombre de las variables usar lowerCamelCase.

Declaring variables: Para la declaración de variables usar las palabras reservadas let y const, no usar var.

Use strict equality: Siempre usar la igualdad o inigualdad estricta.

Function naming: Para el nombre de las funciones usar lowerCamelCase.

Para más información sobre las convenciones de JavaScript se usará como referencia:
https://www.w3schools.com/js/js_conventions.asp

**TypeScript**

Camel case: Usar camelCase cuando nombramos variables y funciones. También se debe usar camelCase en los miembros de una clase y sus métodos. En la interface, el camelCase se usa para nombrar miembros.

Pascal case: Usar pascal case para nombres de clases. En la interface, sirve para nombres.

Para más información sobre las convenciones de TypeScript se usará como referencia:
https://basarat.gitbook.io/typescript/styleguide#array

**Gherkin**

Discernible Given-When-Then Blocks: Se recomienda aplicar sangría a los bloques, para saber cuándo iniciar y terminan.

![](./assets/6.1.3.Source%20Code%20Style%20Guide%20&%20Conventions/Discernible%20Given-When-Then%20Blocks.png)

Steps with Tables: Si necesitamos entrada de una tabla en nuestros pasos, para que sea reconocible, añadiremos dos puntos al final del paso.

![](./assets/6.1.3.Source%20Code%20Style%20Guide%20&%20Conventions/Steps%20with%20Tables.png)

Reducing Noise: Se recomienda usar valores predeterminados para campos que requiere el software pero que no son relevantes para el escenario.

![](./assets/6.1.3.Source%20Code%20Style%20Guide%20&%20Conventions/Reducing%20Noise.png)
 
Parameters in Steps: Para el ejemplo anterior, se pudo notar la inclusión de comillas simples para los parámetros en un paso, lo cual facilita la detección de estos.

Newlines within Scenarios: En caso de que el escenario se está alargando, es recomendable agregar nuevas líneas entre cada paso para que los bloques sean más legibles.

![](./assets/6.1.3.Source%20Code%20Style%20Guide%20&%20Conventions/Newlines%20within%20Scenarios.png)
 
Newlines between scenarios and separator comments: Cuando se tienen muchos escenarios, se vuelve difícil saber el punto donde inicia o termina otro. Por ello, se recomiendo agregar una línea de separación entre escenario y un separador de comentarios.

![](./assets/6.1.3.Source%20Code%20Style%20Guide%20&%20Conventions/Newlines%20between%20scenarios%20and%20separator%20comments.png)


### 6.1.4. Software Deployment Configuration

En esta sección, se detalla la configuración necesaria para llevar a cabo el despliegue satisfactorio de cada uno de los productos digitales en la solución, utilizando herramientas específicas para cada uno de ellos.

**Despliegue de la Landing Page y la Aplicación Web**

Para el despliegue de la Landing Page y la Aplicación Web, se utilizará la plataforma Netlify. A continuación, se detallan los pasos necesarios:

- Configuración del Repositorio: El código fuente de la Landing Page y la Aplicación Web se almacenará en un repositorio en la plataforma Github.
- Creación del Sitio en Netlify: Se creará un nuevo sitio en Netlify vinculado al repositorio que contiene el código fuente de la Landing Page y la Aplicación Web.
- Configuración de Build y Deploy: Netlify proporciona una integración continua (CI/CD) automatizada.
- Configuración de Dominio Personalizado: Opcionalmente, se puede configurar un dominio personalizado para el sitio web desplegado en Netlify.


**Despliegue del Web Service**

Para el despliegue del Web Service, se utilizará la plataforma Railway. A continuación, se detallan los pasos necesarios:

- Configuración del Repositorio: El código fuente del Web Service se almacenará en un repositorio en la plataforma Github.
- Creación del Proyecto en Railway: Se creará un nuevo proyecto en Railway vinculado al repositorio que contiene el código fuente del Web Service.
- Configuración de Variables de Entorno: Railway permite configurar fácilmente variables de entorno para el proyecto. Se configurarán las variables de entorno necesarias, como credenciales de base de datos u otras configuraciones específicas del entorno.
- Despliegue Automatizado: Una vez configurado el proyecto en Railway, se puede habilitar el despliegue automático para que el servicio se actualice automáticamente cada vez que se realicen cambios en el repositorio.
- Monitoreo y Escalado: Railway proporciona herramientas para monitorear el rendimiento del servicio y escalarlo según sea necesario, asegurando un funcionamiento óptimo en todo momento.

**Deployment Diagram de C4 Model**

![](./assets/6.1.4.SoftwareDeploymentConfiguration/+ZTech%20Deployment%20Diagram.png)

## 6.2. Landing Page, Services & Applications Implementation
---
### 6.2.1. Sprint 1
---
#### 6.2.1.1. Sprint Planning 1
| Sprint#        | Sprint 1                      |
|----------------|-------------------------------|
| **Sprint Planning Background** |   |
| Date           | 02/04/2024                    |
| Time           | 11:00 pm                      |
| Location       | Google meet                   |
| Prepared By    | Aldo Pastrana |
| Attendees (to planning meeting) | Sebastian Ramirez / Aldo Pastrana / Pedro Perez / Josue Carrasco / Marzzio Chicana |
| **Sprint n-1 Review Summary** | Este es el primer sprint, no hay reviews anteriores. |
| **Sprint n-1 Retrospective Summary** | El equipo usará Angula para el desarrollo de la Aplicación Web y BootSctrap para el desarrollo del Landing page |
| **Sprint Goal & User Stories** |   |
| Sprint n Goal  | Realizar el desarrollo del Landing Page y Aplicación Web |
| Sprint n Velocity | 10 |
| Sum of story Points | 8 |

#### 6.2.1.2. Sprint Backlog 1
<table>
    <tr>
        <th colspan="1">Sprint #</th>
        <th colspan="5">Sprint n</th>
    </tr>
    <tr>
     <th colspan="2">User Story</th>
        <th colspan="6">Work-Item / Task</th>
    </tr>
    <tr>
        <td>Id</td>
        <td>Title</td>
        <td>Id</td>
        <td>Title</td>
        <td>Description</td>
        <td>Estimation (Hours)</td>
        <td>Assigned To</td>
        <td>Status (To-do / In-Process / To-Review Done)</td>
    </tr>
    <tr>
        <td>US001</td>
        <td>Move between landing page sections</td>
        <td>TK01</td>
        <td>Move between landing page sections</td>
        <td>As a Visitant
I want to move between the sections of the mobile application
So I can see the  functionalities</td>
        <td>1</td>
        <td>Aldo Pastrana</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US002</td>
        <td>View the benefits of the application	</td>
        <td>TK01</td>
        <td>View the benefits of the application	</td>
        <td>As a Visitant
I want to see the benefits that using the application offers,
So you have information to be able to use it.</td>
        <td>1</td>
        <td>Marzzio Chicana</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US003</td>
        <td>View information about company members	</td>
        <td>TK01</td>
        <td>View information about company members	</td>
        <td>As a Visitant
I want to obtain information about the developers of the application,
So I can feel more secure</td>
        <td>1</td>
        <td>Josue Carrasco</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US004</td>
        <td>Collect user contact information via a form	</td>
        <td>TK01</td>
        <td>Collect user contact information via a form	</td>
        <td>As a Visitant,
I want to contact the developers,
So we can have a sales agreement</td>
        <td>1</td>
        <td>Sebastian Ramirez</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US005</td>
        <td>Add new flowerpot	</td>
        <td>TK01</td>
        <td>Add new flowerpot	</td>
        <td>As a Plant Owner
I want to add a new pot to my account in the web application
So I can configure it according to the needs of my plant</td>
        <td>3</td>
        <td>Pedro Perez</td>
        <td>Done</td>
    </tr>
    <tr>
        <td>US012</td>
        <td>Recover password	</td>
        <td>TK01</td>
        <td>Recover password	</td>
        <td>As a Plant Owner
I want to be able to recover my password if it is lost in the web application
So that I do not lose my data or my already made subscriptions.</td>
        <td>3</td>
        <td>Pedro Perez</td>
        <td>Done</td>
    </tr>
</table>

#### 6.2.1.3. Development Evidence for Sprint Review

| Repository          | Branch            | Commit Id | Commit Message           | Commit Message Body                                  | Committed on (Date) |
|---------------------|-------------------|-----------|--------------------------|------------------------------------------------------|---------------------|
| https://github.com/LosChiferos-WS71/ztech-landing-page | main | 9a3460fa33188d95b895d02750e9eaac699cc935  | Add Header | Agregar encabezado | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-landing-page | main | bc30f54238c06628c35569697a521f64fbbfe1e0  | add animate | Agregar animaciones | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-landing-page | main | e065ce648fffc8be412374ecf393eca544858b4d  | feat(add): Update Jquery.min.js | Agregar el Jquery | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-landing-page | main | 76d259212937a87422d07849bc48113e12aa74b5  | Add Main JavaScript | Agregar el main de JavaScript | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-landing-page | main | 568c2a6294696bd95fece6725f07e3f1e2dee815  | update text to english | Actualizar texto a ingles | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-web-application | main | bf09cbdeb2e922b3fda8b3ac3d78e602e746d96c  | feat: Add project basis | Agregar proyecto basse | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-web-application | main | e63f61ebded0c7abfa3c3fdd2b47a010f4c9fe4a  | add register view | Agregar vista de registro | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-web-application | main | 3acc2160e49f47adfd010fad6ff8125fa4afdf83  | Add Application Web | Agregar vista de login | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-web-application | main | 90f78a2b77cbca2ccb9507e72a80e4f926751591  | feat(add): Add component home without css | Agregar component home con CSS | 03/05/2024         |
| https://github.com/LosChiferos-WS71/ztech-web-application | main | 31c2c0791d2a0cfc0ccbb0dfa62dcb7b5232460a  | add register styles | Agregar estilos de la vista registro | 03/05/2024         |

#### 6.2.1.4. Testing Suite Evidence for Sprint Review

Para esta entrega no se ha presentado un backend funcional, se presento un fake API, por lo que los unit tests, integration tests y acceptance tests automaizados, para web services relacionados con los user stories no realizara en esta entrega.

#### 6.2.1.5. Execution Evidence for Sprint Review
>Se realizó el landing page enfocado a nuestra propuesta como startup, evidenciando nuestro compromiso como equipo. 
Las tareas a realizar en cada sprint para la elaboración del landing page fueron:
- Planteamiento y desarrollo sobre nuestros componentes de estrategia empresarial como lo que es la presentacion de las ofertas y ventajas del servicio de ZTech.
-  Ofrecemos una descripción general del servicio, luego detallamos las características específicas del producto, y finalmente presentamos testimonios y un formulario de contacto.
- Presentamos información en secciones bien definidas lo cual facilita la navegación del usuario por áreas de interés específicas.

![](./assets/6.2.1.5.%20Execution%20Evidence%20for%20Sprint%20Review/LandingPage.png)

>Asimismo, se realizo la aplicación web enfocado en el usuario final para ofrecerle un servicio eficaz y de calidad. 
Las tareas a realizar en cada sprint para la elaboración de la aplicación web fueron:
- La interfaz de "Add Flowerpot Maceta" en el cual el usuario podra ingresar el codigo de su maceta para asi registrarlo a su cuenta.

![](./assets/6.2.1.5.%20Execution%20Evidence%20for%20Sprint%20Review/AgregarMaceta.png)

- La interfaz de "Recover your password" en el cual el usuario podra recuperar su contraseña en caso se olvide.

![](./assets/6.2.1.5.%20Execution%20Evidence%20for%20Sprint%20Review/RecuperarContraseña.png)

#### 6.2.1.6. Services Documentation Evidence for Sprint Review
El landing page y aplicación web de nuestro proyecto se realizó utilizando el sistema de versiones de git. El cuál se puede evidenciar el repositorio del proyecto respectivamente:
https://github.com/LosChiferos-WS71/ztech-landing-page 
https://github.com/LosChiferos-WS71/ztech-web-application

- Por otro lado, utilizamos HTML, CSS, JavaScript y BootStrap para realizar la página de nuestro landing page.

![](./assets/6.2.1.6.%20Services%20Documentation%20Evidence%20for%20Sprint%20Review/RepoLandingPage.png)

- Asimismo, utilizamos Angular para realizar las páginas de nuestro aplicación web.

![](./assets/6.2.1.6.%20Services%20Documentation%20Evidence%20for%20Sprint%20Review/RepoAplicacionWeb.png)

#### 6.2.1.7. Software Deployment Evidence for Sprint Review

En este Sprint, se ha completado el despliegue de la landing page y la aplicación web. Esto ha implicado la creación de cuentas, la configuración de recursos en proveedores de nube y la configuración de proyectos de desarrollo para la integración.

Hemos seguido los mismos pasos para los dos despliegues.

1. Crear una cuenta en Netlify:
Acceder a https://www.netlify.com/ y nos creamos una cuenta

<img src="./assets/6.2.1.7 Software Deployment Evidence for Sprint Review/LogIn.jpg" width="700"/>|

2. Conectar Netlify con el repositorio:
En Netlify, hacer clic en "New site".
Seleccionar "Import from Git".
Conectar la cuenta de GitHub.
Seleccionamos el repositorio que contiene nuestra landing page y aplicación web.
Hacer clic en "Deploy site".

<img src="./assets/6.2.1.7 Software Deployment Evidence for Sprint Review/NewSite.jpg" width="700"/>

3. Configurar el sitio web:
Netlify te asignará una URL temporal a nuestro sitio web.

<img src="./assets/6.2.1.7 Software Deployment Evidence for Sprint Review/Config.jpg" width="700"/>

4. Desplegar el sitio web:
Cuando hemos realizado todos los cambios necesarios, hacer clic en "Deploy".

![Deploy](<assets/6.2.1.7 Software Deployment Evidence for Sprint Review/Deploy.jpg>)

#### 6.2.1.8. Team Collaboration Insights during Sprint

**Landing Page**

Hemos desarrollado la implementacion de la Landing Page en ramas de la siguiente manera

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/LandingPageBranches.PNG" width="700"/>

Commits hechos

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/LandingPageCommits.PNG" width="700"/>

Collaboration

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/LandingPageCollaboration.PNG" width="700"/>

**Web App**

Hemos desarrollado la implementacion de la Web App en ramas de la siguiente manera

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/WebAppBranches.PNG" width="700"/>

Commits hechos

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/WebappCommits.PNG" width="700"/>

Collaboration

<img src="./assets/6.2.1.8 Team Collaboration Insights during Sprint/WebAppCollaboration.PNG" width="700"/>


### 6.2.2. Sprint 2

---

#### 6.2.2.1. Sprint Planning 2

---

#### 6.2.2.2. Sprint Backlog 2

---

#### 6.2.2.3. Development Evidence for Sprint Review

---

#### 6.2.2.4. Testing Suite Evidence for Sprint Review

---

#### 6.2.2.5. Execution Evidence for Sprint Review

---

#### 6.2.2.6. Services Documentation Evidence for Sprint Review

---

#### 6.2.2.7. Software Deployment Evidence for Sprint Review

---

#### 6.2.2.8. Team Collaboration Insights during Sprint

---

## 6.3. Validation Interviews

---

### 6.3.1. Diseño de Entrevistas

---

### 6.3.2. Registro de Entrevistas

<img src="./assets/6.3.2. Registro de Entrevistas\Entrevista de validación Jesus.PNG" width="700"/>

https://www.youtube.com/watch?v=ryeC3Tmb6Ms

En esta entrevista, Jesus Sanchez Serna, tiene 23 años. Jesús destaca que la plataforma está excelentemente formulada y equipada con todas las funciones necesarias que uno esperaría. Además, expresa su satisfacción con la landing page, señalando que está muy bien diseñada, permitiendo a los usuarios ver en detalle de lo que trata Ztech. Jesús también hace hincapié en la eficacia de las características de seguridad de la plataforma web, incluyendo un sistema robusto de logeo, registro y recuperación de contraseña, lo cual considera esencial para la protección de la información del usuario. Estos elementos, según él, mejoran la experiencia del usuario y fortalecen la confianza en nuestra plataforma, haciendo que sea una herramienta indispensable para los entusiastas de la jardinería.

### 6.3.3. Evaluaciones según heurísticas

---

## 6.4. Video About-the-Product

---