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
---
## 6.2. Landing Page, Services & Applications Implementation
---
### 6.2.1. Sprint 1
---
#### 6.2.1.1. Sprint Planning 1
---
#### 6.2.1.2. Sprint Backlog 1
---
#### 6.2.1.3. Development Evidence for Sprint Review
---
#### 6.2.1.4. Testing Suite Evidence for Sprint Review
---
#### 6.2.1.5. Execution Evidence for Sprint Review
---
#### 6.2.1.6. Services Documentation Evidence for Sprint Review
---
#### 6.2.1.7. Software Deployment Evidence for Sprint Review
---
#### 6.2.1.8. Team Collaboration Insights during Sprint
---