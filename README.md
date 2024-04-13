### Universidad Peruana de Ciencias Aplicadas
### SI572 | WS71 | Desarrollo de Soluciones IoT
### Profesor: Angel Augusto Velasquez Nuñez
### Ingeniería de Software
.
# ZTech
### TB1 REPORT - LOS CHIFEROS
================================
#### Team members
- Chicana Romero, Marzzio Braulio (U202022228)
- Pastrana León, Aldo Francisco (U20211C186)
- Carrasco Hernandez, Florentino Josue (U202020727)
- Ramirez Zapata, Sebastián Jesús (U20201C031)
- Perez Pizarro, Pedro Jeremy (U202022237)

#### Ciclo 2024-01

---
# Registro de Versiones del Informe
| <div style="width: 50px">Versión</div> | <div style="width: 80px">Fecha</div> | <div style="width: 80px">Autor</div> | Descripción de modificación |
|:---------:|:-------:|:-------:|-----------------------------|
| **v1.1** | 04-04-2024 | Los Chiferos | Para esta versión, hemos priorizado los capítulos que abordan directamente la startup, el problema a resolver y el producto que se planea desarrollar. Además, hemos definido con mayor claridad los segmentos objetivos y hemos llevado a cabo un proceso de investigación para identificar las necesidades del mercado, conocido como "needfinding". |
| **v1.2** | 08-04-2024 | Los Chiferos | Para esta versión, hemos procedido a actualizar los user persona centrándonos en los resultados de nuestras entrevistas. Además, el equipo llevó a cabo una sesión de "event storming" con el fin de definir el dominio y los contextos acotados de nuestra solución. |
| **v1.3** | 13-04-2024 | Los Chiferos | Para esta versión, hemos desarrollado la arquitectura de software utilizando diagramas de contexto y contenedores. Además, hemos llevado a cabo una exhaustiva verificación de errores y hemos actualizado puntos previamente identificados. |
---
# Project Report Collaboration Insights
---
# Contenido
- [Capítulo I: Introducción](/chapter01.md#capítulo-i-introducción)
  - [1.1. Startup Profile](/chapter01.md#11-startup-profile)
    - [1.1.1. Descripción de la Startup](/chapter01.md#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](/chapter01.md#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](/chapter01.md#12-solution-profile)
    - [1.2.1 Antecedentes y problemática](/chapter01.md#121-antecedentes-y-problemática)
    - [1.2.2 Lean UX Process](/chapter01.md#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](/chapter01.md#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](/chapter01.md#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hypothesis Statements](/chapter01.md#1223-lean-ux-hypothesis-statements)
      - [1.2.2.4. Lean UX Canvas](/chapter01.md#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](/chapter01.md#13-segmentos-objetivo)
- [Capítulo II: Requirements Elicitation \& Analysis](/chapter02.md#capítulo-ii-requirements-elicitation--analysis)
  - [2.1. Competidores](/chapter02.md#21-competidores)
    - [2.1.1. Análisis competitivo](/chapter02.md#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](/chapter02.md#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](/chapter02.md#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](/chapter02.md#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](/chapter02.md#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](/chapter02.md#223-análisis-de-entrevistas)
  - [2.3. Needfinding](/chapter02.md#23-needfinding)
    - [2.3.1. User Personas](/chapter02.md#231-user-personas)
    - [2.3.2. User Task Matrix](/chapter02.md#232-user-task-matrix)
    - [2.3.3. User Journey Mapping](/chapter02.md#233-user-journey-mapping)
    - [2.3.4. Empathy Mapping](/chapter02.md#234-empathy-mapping)
    - [2.3.5. As-is Scenario Mapping](/chapter02.md#235-as-is-scenario-mapping)
  - [2.4. Ubiquitous Language](/chapter02.md#24-ubiquitous-language)
- [Capítulo III: Requirements Specification](/chapter03.md#capítulo-iii-requirements-specification)
  - [3.1. To-Be Scenario Mapping](/chapter03.md#31-to-be-scenario-mapping)
  - [3.2. User Stories](/chapter03.md#32-user-stories)
  - [3.3. Impact Mapping](/chapter03.md#33-impact-mapping)
  - [3.4. Product Backlog](/chapter03.md#34-product-backlog)
- [Capítulo IV: Solution Software Design](/chapter04.md#capítulo-iv-solution-software-design)
  - [4.1. Strategic-Level Domain-Driven Design](/chapter04.md#41-strategic-level-domain-driven-design)
    - [4.1.1. EventStorming](/chapter04.md#411-eventstorming)
      - [4.1.1.1 Candidate Context Discovery](/chapter04.md#4111-candidate-context-discovery)
      - [4.1.1.2 Domain Message Flows Modeling](/chapter04.md#4112-domain-message-flows-modeling)
      - [4.1.1.3 Bounded Context Canvases](/chapter04.md#4113-bounded-context-canvases)
    - [4.1.2. Context Mapping](/chapter04.md#412-context-mapping)
    - [4.1.3. Software Architecture](/chapter04.md#413-software-architecture)
      - [4.1.3.1. Software Architecture System Landscape Diagram](/chapter04.md#4131-software-architecture-system-landscape-diagram)
      - [4.1.3.2. Software Architecture Context Level Diagrams](/chapter04.md#4132-software-architecture-context-level-diagrams)
      - [4.1.3.3. Software Architecture Container Level Diagrams](/chapter04.md#4133-software-architecture-container-level-diagrams)
      - [4.1.3.4. Software Architecture Deployment Diagrams](/chapter04.md#4134-software-architecture-deployment-diagrams)
  - [4.2. Tactical-Level Domain-Driven Design](/chapter04.md#42-tactical-level-domain-driven-design)
    - [4.2.X. Bounded Context: ](/chapter04.md#42x-bounded-context-)
      - [4.2.X.1. Domain Layer](/chapter04.md#42x1-domain-layer)
      - [4.2.X.2. Interface Layer](/chapter04.md#42x2-interface-layer)
      - [4.2.X.3. Application Layer](/chapter04.md#42x3-application-layer)
      - [4.2.X.4. Infrastructure Layer](/chapter04.md#42x4-infrastructure-layer)
      - [4.2.X.5. Bounded Context Software Architecture Component Level Diagrams](/chapter04.md#42x5-bounded-context-software-architecture-component-level-diagrams)
      - [4.2.X.6. Bounded Context Software Architecture Code Level Diagrams](/chapter04.md#42x6-bounded-context-software-architecture-code-level-diagrams)
        - [4.2.X.6.1. Bounded Context Domain Layer Class Diagrams](/chapter04.md#42x61-bounded-context-domain-layer-class-diagrams)
        - [4.2.X.6.2. Bounded Context Database Design Diagram](/chapter04.md#42x62-bounded-context-database-design-diagram)
- [Avance de Conclusiones, Bibliografía y Anexos](/conclusions_bibliography_annexes.md#avance-de-conclusiones-bibliografía-y-anexos)
---

# Student Outcome
---