# Capítulo IV: Solution Software Design
---
## 4.1. Strategic-Level Domain-Driven Design
---
### 4.1.1. EventStorming
EventStoring es una técnica de modelado colaborativa e iterativa para simular un área problemática grande y compleja, lo que permite ahondar en la mayor cantidad de detalles y problemas posibles.
#### 4.1.1.1 Candidate Context Discovery
---  
**Step 1: Unstructured Exploration**  
Como primer paso del EventStoring comenzamos con una sesión de lluvia de ideas sobre los eventos del dominio relacionados con el negocio estudiado. Es importante formar los acontecimientos del dominio en tiempo pasado los cuales describen lo sucedido.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step1%20-Unstructured%20Exploration.png)

---
**Step 2: Timelines**  
Luego como segundo paso, revisamos los eventos de dominio generados y los organizamos en el orden en que ocurren en el dominio. Es decir, los eventos deben comenzar con un happy path los cuales describen un escenario comercial exitoso. Finalmente, una vez que se completa el happy path, se pueden agregar escenarios alternativos.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%202%20-%20Timelines.png)

---
**Step 3: Paint Points**  
Después de organizar los eventos en una línea de tiempo, usamos esta vista amplia para identificar puntos de interés a lo largo del camino. Tales como los cuellos de botella, pasos manuales que requieren automatización, falta de documentación o falta de conocimiento del dominio.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%203%20-Paint%20Points.png)

---
**Step 4: Pivotal Points**  
Una vez terminado nuestra línea de eventos completo con paint points, buscamos eventos comerciales clave que indiquen un cambio en el contexto o la fase. Estos se denominan eventos principales los cuales los marcamos con una barra vertical que separa los eventos anteriores y posteriores al evento principal.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%204%20-Pivotal%20Points.png)

---
**Step 5: Commands**  
En este paso los comandos describen la causa del evento o el flujo de eventos. Es decir, los comandos describen las operaciones del sistema, diferenciándose de los eventos de dominio, se construyen en imperativo.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%205-%20Commands.png)

---
**Step 6: Policies**  
En este punto, buscamos reglas de automation policies que puedan ejecutar estos comandos. Es decir, una automation policy es un escenario en el que un evento desencadena la ejecución de un comando. En otras palabras, el comando se ejecuta automáticamente cuando ocurre un evento específico del dominio.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%206-%20Policies.png)0

---
**Step 7: Read Models**  
En este paso, el modelo de lectura es la representación de datos en el dominio que el agente utiliza para decidir si ejecuta o no el comando. Es por eso, que definimos una vista de datos por cada comando tales como los monitores del sistema, informes, notificaciones y entre otros.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%207-Read%20Models.png)

---
**Step 8: External Systems**  
Este paso completamos el modelo con sistemas externos. Es decir, un sistema externo se define como cualquier sistema que no forma parte del dominio que se está trabajando. Además, puede ejecutar comandos (entrar) o recibir notificaciones sobre eventos (salir).

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%208-External%20Systems.png)

---
**Step 9: Aggregates**  
Después de haber presentado todos los eventos y comandos, comenzamos a pensar en agrupar los conceptos relacionados en agregados los cuales reciben comandos y generan eventos.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%209-Aggregates.png)

---
**Step 10: Bounded Contexts**  
Como último paso buscamos agregados que sea relacionen y sean relevantes entre sí porque representan funciones estrechamente relacionadas o porque están relacionadas según políticas. Es decir, los grupos de agregados generan candidatos naturales para los límites de los contextos delimitados.

![](./assets/4.1.1.1%20Candidate%20Context%20Discovery/Step%2010-Bounded%20Contexts.png)

#### 4.1.1.2 Domain Message Flows Modeling
Un Domain Message Flow Diagram es una visualización simple que muestra el flujo de mensajes (commands, events, queries) entre actors, bounded contexts y systems para un escenario.

---
**Scenario: Register and Set Up Pots Correctly**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Register%20and%20Set%20Up%20Pots%20Correctly.png)

---
**Scenario: Generate a Claim for a Defective Flowerpot**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Generate%20a%20Claim%20for%20a%20Defective%20Flowerpot.png)

---
**Scenario: Subscription not Renewed**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Subscription%20not%20Renewed.png)

---
**Scenario: Scenario: Account creation and verification**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Account%20creation%20and%20verification.png)

---
**Scenario: Sort Order Stock for Inventory**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Sort%20Order%20Stock%20for%20Inventory.png)

---
**Scenario: Process Order Replenishment**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Process%20Order%20Replenishment.png)

---
**Scenario: Start Sensors to Collect Data**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling//Scenario%20Start%20Sensors%20to%20Collect%20Data.png)

---
**Scenario: Calculate and Send Metrics**

![](./assets/4.1.1.2%20Domain%20Message%20Flows%20Modeling/Scenario%20Calculate%20and%20Send%20Metrics.png)

#### 4.1.1.3 Bounded Context Canvases
Bounded Context Canvas es una herramienta colaborativa para diseñar y documentar un único proyecto de contexto limitado. Un contexto restringido es un subsistema en una arquitectura de software que está asociado con una parte de su dominio. Canvas lo guía a través de un proceso de diseño contextual limitado, pidiéndole que revise y tome decisiones sobre los elementos clave del diseño, desde la denominación hasta las responsabilidades, las interfaces públicas y las dependencias.

---
**Account Context**

![](./assets/4.1.1.3%20Bounded%20Context%20Canvases/Account%20Context.png)

---
**Flowerpot Context**

![](./assets/4.1.1.3%20Bounded%20Context%20Canvases/Flowerpot%20Context.png)

---
**Inventory Context**

![](./assets/4.1.1.3%20Bounded%20Context%20Canvases/Inventory%20Context.png)

---
**Claim Context**

![](./assets/4.1.1.3%20Bounded%20Context%20Canvases/Claim%20Context.png)

---
**IoT Solution Context**

![](./assets/4.1.1.3%20Bounded%20Context%20Canvases/IoT%20Solution%20Context.png)

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
### 4.2.X. Bounded Context: <Bounded Context Name>
---
#### 4.2.X.1. Domain Layer
---
#### 4.2.X.2. Interface Layer
---
#### 4.2.X.3. Application Layer
---
#### 4.2.X.4. Infrastructure Layer
---
#### 4.2.X.5. Bounded Context Software Architecture Component Level Diagrams
---
#### 4.2.X.6. Bounded Context Software Architecture Code Level Diagrams
---
##### 4.2.X.6.1. Bounded Context Domain Layer Class Diagrams
---
##### 4.2.X.6.2. Bounded Context Database Design Diagram
---