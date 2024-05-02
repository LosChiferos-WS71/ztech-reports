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
### 4.2.3. Bounded Context: Flowerpot

En el contexto de Flowerpot, los dueños de las macetas pueden gestionar sus pedidos, configurar sus macetas, y recibir informes sobre el estado de sus plantas. Este Bounded Context abarca desde el inicio del pedido hasta el seguimiento y reporte del estado y salud de las plantas.

---
#### 4.2.3.1. Domain Layer
**Entities**: `Pot`, `Order`, `Report`, `PotConfiguration`, `Subscription`.

**Value Objects**: `PotStatus`, `ConfigurationData`, `ReportData`.

**Aggregates**: `PotOrder` que incluye `Pot`, `PotConfiguration`, y `Subscription`.

**Repositories**: `PotRepository`, `OrderRepository`, `ReportRepository` para la persistencia de datos.

**Domain Services**: `PotManagementService` para operaciones relacionadas con las macetas y su estado.

---
#### 4.2.3.2. Interface Layer

**API Endpoints**: Rutas como POST `/orders/pot` para nuevos pedidos, GET `/reports/{id}` para consultar informes.

**DTOs**: `OrderDTO`, `PotConfigurationDTO`, `ReportDTO` para la estructura de datos intercambiados.

**Controllers**: `PotController`, `OrderController`, `ReportController` para manejar solicitudes API y delegar a la capa de aplicación.

---
#### 4.2.3.3. Application Layer

**Application Services**: `PotOrderApplicationService` que maneja la lógica de creación, seguimiento y procesamiento de pedidos de macetas.

**Commands/Queries**: `CreatePotOrderCommand`, `GenerateReportQuery`.

**Command Handlers**: `CreatePotOrderHandler`, `GenerateReportHandler`.

---
#### 4.2.3.4. Infrastructure Layer

**Repository Implementation**: Como `PotRepositorySQL` para las interacciones con la base de datos de macetas.

**External Services**: Integraciones con proveedores de sensores, servicios de mensajería para notificaciones, y plataforma externa de pago para gestionar suscripciones.

**Factories**: Para la creación de instancias complejas de entidades y agregados.

**ORM / Database Access**: Utilización de herramientas para mapear objetos a registros de base de datos.

---
#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams

![C4 component Flowerpot](assets/componentflowerpot.png)

---
#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams
![Bounded Context Class Design Diagram](assets/class3.png)

---
##### 4.2.3.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](assets/database3.png)

---