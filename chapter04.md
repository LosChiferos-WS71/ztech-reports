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
## 4.2.1.1. Domain Layer

**Entities:** Incluyen clases como `Account`, `User`, `PlantOwner`, y `Provider`. Cada entidad tiene sus propios atributos y comportamientos que definen qué es y qué puede hacer. `User` podría extenderse a `VerifiedUser` y `UnverifiedUser`.

**Value Objects:** Objetos inmutables que tienen atributos pero no identidad distinta, como `Address` o `SensorData`.

**Aggregates:** Un conjunto de objetos asociados que se tratan como una unidad única, por ejemplo, un agregado `Account` que incluye `User`, `UserState`, y `PlantSensorInfo`.

**Repositories:** Abstracciones para el acceso a los objetos del dominio, como `AccountRepository` o `PlantInfoRepository`.

**Services:** Incluyen servicios del dominio para operaciones que no pertenecen naturalmente a ninguna entidad, como `VerificationService` o `AccountCreationService`.

---

## 4.2.1.2. Interface Layer

**API Endpoints:** Rutas REST para manejar la creación de cuentas y los procesos de verificación, como POST `/accounts` para la creación de cuentas y PUT `/accounts/{id}/verify` para la verificación de cuentas.

**DTOs:** Objetos de transferencia de datos como `AccountCreationRequest` y `VerificationRequest` que definen la estructura de datos para las solicitudes.

**View Models:** Para enviar datos a vistas o APIs externas, como `AccountDetailsViewModel`.

**Controllers:** Que llaman a servicios de aplicación, como `AccountController` que maneja las solicitudes HTTP y delega a los servicios de aplicación.

---

## 4.2.1.3. Application Layer

**Services:** Servicios de aplicación que orquestan los servicios de dominio e interacciones de repositorio, como `AccountApplicationService` que maneja la lógica de registro y verificación de cuentas.

**Commands/Queries:** Objetos que encapsulan datos necesarios para realizar acciones, como `CreateAccountCommand` o `VerifyAccountCommand`.

**Command Handlers:** Manejan los comandos, como `CreateAccountHandler`.

**Event Handlers:** Responden a eventos del dominio, como cuando una cuenta es verificada.

---

## 4.2.1.4. Infrastructure Layer

**Persistence Mechanisms:** Implementaciones de los repositorios que interactúan con la base de datos, como `AccountSQLRepository`.

**External Service Integrations:** Tales como la comunicación con el sistema SUNAT para validación o integración con proveedores de datos de sensores.

**Factories:** Para la creación de objetos de dominio complejos.

**API Clients:** Para interactuar con otros bounded contexts o servicios externos.

---
#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams

![C4 Component Diagram](/assets/componentAccount.png)

--- 
#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

![Bounded Context Class Design Diagram](/assets/class1.png)


---
##### 4.2.1.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](/assets/Profile_Bounded_Context_Database.png)

---

