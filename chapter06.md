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
---
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