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
### 4.2.2. Bounded Context: Inventory
La gestión de inventario es crucial en la operación de empresas que requieren mantener un registro actualizado de los artículos disponibles, así como la coordinación efectiva con los proveedores. Este contexto delimitado maneja desde el pedido inicial de suministros hasta la actualización y consulta del historial de órdenes y del inventario.
---
#### 4.2.2.1. Domain Layer

**Entidades**: `Pedido`, `ArtículoInventario`, `ActualizaciónInventario`, `HistorialPedido`.

**Objetos de Valor**: `Cantidad`, `InformaciónProducto`, `EstadoPedido`.

**Agregados**: `Pedido` que incluye `ArtículoInventario` y `EstadoPedido`.

**Repositorios**: `RepositorioPedido`, `RepositorioInventario` para acceso y manipulación de los datos.

**Servicios de Dominio**: `ServicioGestiónStock` para operaciones de actualización y mantenimiento del inventario.

---
#### 4.2.2.2. Interface Layer

**API Endpoints**: Rutas como POST `/pedidos` para nuevos pedidos, GET `/inventario` para consulta de inventario.

**DTOs**: `PedidoDTO`, `ArtículoInventarioDTO` para la estructura de datos intercambiados.

**Controladores**: `ControladorPedido`, `ControladorInventario` para manejar solicitudes API y delegar a la capa de aplicación.

---
#### 4.2.2.3. Application Layer

**Servicios de Aplicación**: `ServicioAplicaciónPedido` que maneja la lógica de creación y procesamiento de pedidos.

**Comandos/Consultas**: `CrearPedidoComando`, `ConsultarInventarioConsulta`.

**Manejadores de Comandos**: `CrearPedidoManejador`, `ActualizarInventarioManejador`.

---
#### 4.2.2.4. Infrastructure Layer
**Implementación de Repositorios**: Como `RepositorioPedidoSQL` para interacciones con la base de datos.

**Servicios Externos**: Integración con sistemas de proveedores para pedidos y actualización de inventario.

**Factories**: Creación de instancias de agregados o entidades.

**ORM / Acceso a la Base de Datos**: Herramientas para mapear objetos a registros de base de datos.

---
#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams
---
#### 4.2.2.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams
![Bounded Context Database Design Diagram](assets/class2.png)

---
##### 4.2.2.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](assets/database2.png)

---