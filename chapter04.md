# Capítulo IV: Solution Software Design
---
## 4.1. Strategic-Level Domain-Driven Design
---
### 4.1.1. EventStorming
---
#### 4.1.1.1 Candidate Context Discovery
---
#### 4.1.1.2 Domain Message Flows Modeling
---
#### 4.1.1.3 Bounded Context Canvases
---
### 4.1.2. Context Mapping
---
### 4.1.3. Software Architecture
---
#### 4.1.3.1. Software Architecture System Landscape Diagram
---
#### 4.1.3.2. Software Architecture Context Level Diagrams
---
#### 4.1.3.3. Software Architecture Container Level Diagrams
---
#### 4.1.3.4. Software Architecture Deployment Diagrams
---
## 4.2. Tactical-Level Domain-Driven Design
---
### 4.2.1. Bounded Context: Account 
---
#### 4.2.1.1. Domain Layer

**Entidades:** Incluyen clases como Cuenta, Usuario, PropietarioPlanta, y Proveedor. Cada entidad tiene sus propios atributos y comportamientos que definen qué es y qué puede hacer. Usuario podría extenderse a UsuarioVerificado y UsuarioNoVerificado. 

**Objetos de Valor:** Objetos inmutables que tienen atributos pero no identidad distinta, como Dirección o DatosSensor.

**Agregados:** Un conjunto de objetos asociados que se tratan como una unidad única, por ejemplo, un agregado Cuenta que incluye Usuario, EstadoUsuario, y InformacionSensorPlanta.

**Repositorios:** Abstracciones para el acceso a los objetos del dominio, como RepositorioCuenta o RepositorioInformacionPlanta.

**Servicios:** Incluyen servicios del dominio para operaciones que no pertenecen naturalmente a ninguna entidad, como ServicioVerificación o ServicioCreaciónCuenta.

---
#### 4.2.1.2. Interface Layer

**Puntos de API:** Rutas REST para manejar la creación de cuentas y los procesos de verificación, como POST `/cuentas` para la creación de cuentas y PUT `/cuentas/{id}/verificar` para la verificación de cuentas.

**DTOs:** Objetos de transferencia de datos como `SolicitudCreacionCuenta` y `SolicitudVerificacionCuenta` que definen la estructura de datos para las solicitudes.

**Modelos de Vista:** Para enviar datos a vistas o APIs externas, como `ModeloVistaDetallesCuenta`.

**Controladores:** Que llaman a servicios de aplicación, como `ControladorCuenta` que maneja las solicitudes HTTP y delega a los servicios de aplicación.

---
#### 4.2.1.3. Application Layer
**Servicios:** Servicios de aplicación que orquestan los servicios de dominio e interacciones de repositorio, como `ServicioAplicacionCuenta` que maneja la lógica de registro y verificación de cuentas.

**Comandos/Consultas:** Objetos que encapsulan datos necesarios para realizar acciones, como `ComandoCrearCuenta` o `ComandoVerificarCuenta`.

**Manejadores de Comandos:** Manejan los comandos, como `ManejadorComandoCrearCuenta`.

**Manejadores de Eventos:** Responden a eventos del dominio, como cuando una cuenta es verificada.

---
#### 4.2.1.4. Infrastructure Layer

**Mecanismos de Persistencia:** Implementaciones de los repositorios que interactúan con la base de datos, como `RepositorioCuentaSQL`.

**Integraciones de Servicios Externos:** Tales como la comunicación con el sistema SUNAT para validación o integración con proveedores de datos de sensores.

**Fábricas:** Para la creación de objetos de dominio complejos.

**Clientes API:** Para interactuar con otros bounded contexts o servicios externos.

---
#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams
--- 
#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

![Bounded Context Class Design Diagram](/assets/boudedclases1.png)


---
##### 4.2.1.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](/assets/Bounded1.png)

---

