# Capítulo VI: Product Implementation, Validation & Deployment
---
## 6.1. Software Configuration Management
---
### 6.1.1. Software Development Environment Configuration
---
### 6.1.2. Source Code Management
---
### 6.1.3. Source Code Style Guide & Conventions
---
### 6.1.4. Software Deployment Configuration
---
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
---
#### 6.2.1.8. Team Collaboration Insights during Sprint
---