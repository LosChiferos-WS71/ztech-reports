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
### 4.2.5. Bounded Context: IOT Solution
El Bounded Context de "IoT Solution" se centra en la solución integral de Internet de las Cosas (IoT) para la gestión de datos de macetas inteligentes. Cubre la recolección de datos ambientales, su procesamiento y la transmisión de métricas, lo que permite a los propietarios de plantas monitorizar y ajustar las condiciones de sus macetas para un óptimo crecimiento de las plantas.

---
#### 4.2.5.1. Domain Layer

**Entidades**: `Sensor`, `Metric`, `DataPoint`.

**Objetos de Valor**: `HumidityValue`, `SunlightValue`, `TemperatureValue`.

**Agregados**: `SensorData` que incluye lecturas de `Humidity`, `Sunlight`, y `Temperature`.

**Repositorios**: `SensorRepository`, `MetricRepository` para la persistencia y recuperación de datos de sensores y métricas.

**Servicios de Dominio**: `DataCollectionService` que define cómo se recopilan y procesan los datos de los sensores.

---
#### 4.2.5.2. Interface Layer
**API Endpoints**: Rutas como GET `/metrics/{sensorId}` para obtener métricas y POST `/data` para la entrada de nuevos datos de sensores.

**DTOs**: `SensorDataDTO`, `MetricDTO` para la estructura de datos intercambiados.

**Controladores**: `SensorController`, `MetricController` para manejar solicitudes API y delegar a la capa de aplicación.

---
#### 4.2.5.3. Application Layer
**Servicios de Aplicación**: `MetricProcessingService` para la lógica de cómo se calculan y envían las métricas.

**Comandos/Consultas**: `ProcessSensorDataCommand`, `RetrieveMetricsQuery`.

**Manejadores de Comandos**: `ProcessSensorDataHandler`, `RetrieveMetricsHandler`.

---
#### 4.2.5.4. Infrastructure Layer
**Implementación de Repositorios**: Como `SQLSensorRepository` para la interacción con la base de datos.

**Servicios Externos**: Integraciones con servicios en la nube para el almacenamiento y análisis de datos a gran escala.

**Factories**: Para la creación de instancias complejas de datos de sensores y métricas.

**ORM / Acceso a la Base de Datos**: Herramientas para mapear entidades a registros de base de datos, como Entity Framework o Hibernate.

---
#### 4.2.5.5. Bounded Context Software Architecture Component Level Diagrams
---
#### 4.2.5.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.5.6.1. Bounded Context Domain Layer Class Diagrams

![Bounded Context Class Design Diagram](/assets/class5.png)

---
##### 4.2.5.6.2. Bounded Context Database Design Diagram

![Bounded Context Database Design Diagram](/assets/database5.png)

---