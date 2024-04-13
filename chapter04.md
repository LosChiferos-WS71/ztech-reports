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
**Entidades**: `Maceta`, `Pedido`, `Informe`, `ConfiguraciónMaceta`, `Suscripción`.

**Objetos de Valor**: `EstadoMaceta`, `DatosConfiguración`, `DatosInforme`.

**Agregados**: `PedidoMaceta` que incluye `Maceta`, `ConfiguraciónMaceta`, y `Suscripción`.

**Repositorios**: `RepositorioMaceta`, `RepositorioPedido`, `RepositorioInforme` para la persistencia de datos.

**Servicios de Dominio**: `ServicioGestiónMacetas` para operaciones relacionadas con las macetas y su estado.

---
#### 4.2.3.2. Interface Layer

**API Endpoints**: Rutas como POST `/pedidos/maceta` para nuevos pedidos, GET `/informes/{id}` para consultar informes.

**DTOs**: `PedidoDTO`, `ConfiguraciónMacetaDTO`, `InformeDTO` para la estructura de datos intercambiados.

**Controladores**: `ControladorMaceta`, `ControladorPedido`, `ControladorInforme` para manejar solicitudes API y delegar a la capa de aplicación.

---
#### 4.2.3.3. Application Layer

**Servicios de Aplicación**: `ServicioAplicaciónPedidoMaceta` que maneja la lógica de creación, seguimiento y procesamiento de pedidos de macetas.

**Comandos/Consultas**: `CrearPedidoMacetaComando`, `GenerarInformeConsulta`.

**Manejadores de Comandos**: `CrearPedidoMacetaManejador`, `GenerarInformeManejador`.

---
#### 4.2.3.4. Infrastructure Layer

**Implementación de Repositorios**: Como `RepositorioMacetaSQL` para las interacciones con la base de datos de macetas.

**Servicios Externos**: Integraciones con proveedores de sensores, servicios de mensajería para notificaciones, y plataforma externa de pago para gestionar suscripciones.

**Factories**: Para la creación de instancias complejas de entidades y agregados.

**ORM / Acceso a la Base de Datos**: Utilización de herramientas para mapear objetos a registros de base de datos.

---
#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams
---
#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams
![Bounded Context Class Design Diagram](assets/class3.png)

---
##### 4.2.3.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](assets/database3.png)

---