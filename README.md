# VALHALLA VAULT - Digital Banking Platform
> **Enterprise Banking Core y Secure Financial Architecture**

<p align="center">
  <img src="./assets/images/logo.png" alt="Valhalla Vault Logo" width="250">
</p>

## 📌 Nota sobre el Proyecto
**Valhalla Vault** es un concepto de plataforma de banca digital fullstack en desarrollo, concebido exclusivamente con fines educativos y de aprendizaje personal para mi portafolio profesional. El nombre y la identidad visual están inspirados en la **mitología nórdica**, representando la fortaleza, la custodia de activos y la protección inexpugnable de una bóveda financiera.

> ⚠️ **Nota de evolución:** Este `README.md` es un documento dinámico que se irá actualizando a medida que el proyecto avance y se completen las distintas etapas. Toda la documentación detallada, diagramas de arquitectura y decisiones de diseño se irán almacenando progresivamente en la carpeta `/docs`.

---

## 🏛️ Visión Técnica
La plataforma está proyectada como un sistema bancario digital *Fullstack* evolutivo. Su propósito es simular un núcleo transaccional real diseñado para escalar progresivamente desde un prototipo local ejecutable en consola hasta una arquitectura empresarial distribuida basada en microservicios, comunicación asíncrona por eventos y principios de *Clean y Hexagonal Architecture*.

---

## 🌿 Estrategia de Ramas (Git Branching Strategy)
Para mantener un historial de desarrollo limpio y organizado, **cada hito técnico del producto se desarrollará en su propia rama (*branch*) dedicada**:

- `main`: Versión estable e integrada del sistema.
- `feature/v0.1-banking-core`: Fase 1 — Modelo de dominio y reglas financieras básicas (`v0.1`).
- `feature/v0.4-backend-api`: Fase 2 — Persistencia en PostgreSQL, APIs REST en Spring Boot, JWT y servicio en Node.js (`v0.4`).
- `feature/v0.6-angular-experience`: Fase 3 — Interfaz web interactiva en Angular 17+ y conexión a APIs (`v0.6`).
- `feature/v0.7-clean-architecture`: Fase 4 — Refactorización con SOLID, Clean/Hexagonal Architecture y ADRs (`v0.7`).
- `feature/v1.0-fullstack-delivery`: Fase 5 — Integración End-to-End, Swagger, Docker, CI/CD y despliegue (`v1.0`).
- `feature/v1.1-ai-assisted`: Fase 6 — Flujos de ingeniería aumentados con IA y validación técnica (`v1.1`).
- `feature/v1.2-hardening-observability`: Fase 7 — Hardening, OWASP, testing avanzado, observabilidad y resiliencia (`v1.2`).
- `feature/v2.0-scalable-architecture`: Fase 8 — Domain-Driven Design (DDD), Bounded Contexts y RabbitMQ (`v2.0`).
- `feature/v3.0-global-design`: Fase 9 — System Design global, Vertical Slice y arquitectura distribuida (`v3.0`).

---

## 🛠️ Tech Stack Principal

- **Backend Core:** Java 17+, Spring Boot 3+ (Spring Web, Spring Data JPA, Spring Security).
- **Servicios Complementarios:** Node.js, TypeScript (Valhalla Notification Service).
- **Frontend Experience:** Angular 17+, TypeScript, RxJS, HTML5, CSS3/SASS.
- **Base de Datos y Persistencia:** PostgreSQL, Hibernate / JPA, SQL DDL/DML, Transacciones ACID.
- **Seguridad y Autenticación:** JWT (JSON Web Tokens), BCrypt Hashing, RBAC (Role-Based Access Control).
- **Infraestructura y DevOps:** Docker, Docker Compose, GitHub Actions (CI/CD), OpenAPI / Swagger.
- **Arquitectura y Patrones:** Domain-Driven Design (DDD), Clean & Hexagonal Architecture (Ports & Adapters), Event-Driven Architecture (RabbitMQ/Message Broker).
- **AI Engineering:** Cursor AI (Prompt Engineering técnico, debugging y refactoring asistido).

---

## 🗺️ Roadmap de Arquitectura Evolutiva

### 🟢 Fase 1: Domain Core & Financial Rules (`v0.1`)
- **Modelado del Dominio Financiero:** Abstracción y encapsulamiento de entidades (`Customer`, `Account`, `Transaction`).
- **Reglas Financieras Básicas:** Validación de saldos, control de límites operativos y cálculo de comisiones.
- **Consola Transaccional:** Registro e historial de depósitos, retiros y transferencias con manejo estructurado de excepciones.

### 🟡 Fase 2: Core Persistence & REST Services (`v0.4`)
- **Persistencia Relacional:** Diseño del modelo Entidad-Relación en PostgreSQL con integridad referencial y soporte ACID.
- **REST APIs & Spring Boot:** Desarrollo de servicios expuestos en Spring Boot para operaciones bancarias.
- **Seguridad JWT:** Configuración de filtros con Spring Security, cifrado de credenciales y autorización por roles (`CUSTOMER`, `EMPLOYEE`, `ADMINISTRATOR`, `AUDITOR`).
- **Microservicio Secundario:** Integración con un servicio de notificaciones en Node.js y TypeScript.

### 🔵 Fase 3: Digital Experience & SPA (`v0.6`)
- **Estructura Web y Responsive Design:** Creación de un Dashboard interactivo adaptado a dispositivos móviles y escritorio.
- **SPA con Angular:** Componentes reactivos, consumo de servicios con RxJS, `Guards` de navegación e `Interceptors` para el token JWT.
- **Flujos Integrados:** Autenticación, consulta de extractos, registro de beneficiarios y envío de dinero.

### 🔴 Fase 4: Clean Architecture & Decoupling (`v0.7`)
- **Separación de Responsabilidades:** Refactorización aplicando principios SOLID y patrones de diseño (*Repository*, *Factory*, *Adapter*).
- **Clean & Hexagonal Architecture:** Aislamiento del dominio del negocio mediante *Ports & Adapters*.
- **Gobierno Arquitectónico:** Registro formal de decisiones de diseño mediante *Architecture Decision Records* (ADRs).

### 🟠 Fase 5: End-to-End Delivery & DevOps (`v1.0`)
- **Integración Fullstack:** Conexión de todo el ciclo operativo (Frontend → API → Backend → Base de Datos → Servicios).
- **Documentación de APIs:** Especificación del contrato del banco utilizando OpenAPI / Swagger.
- **DevOps & Delivery:** Containerización con Docker/Docker Compose, pipelines de CI/CD con GitHub Actions y despliegue en la nube.

### 🟣 Fase 6: AI-Assisted Development & Optimization (`v1.1`)
- **Ingeniería Aumentada:** Uso profesional de herramientas de IA proporcionando contexto de arquitectura y restricciones de negocio.
- **Debugging y Refactoring:** Identificación de causas raíz, mitigación de code smells y refactorización guiada.
- **Testing y Cuestionamiento:** Generación asistida de escenarios de prueba extremos (*edge cases*) con validación técnica humana.

### 🛡️ Fase 7: Hardening, Observability & Resilience (`v1.2`)
- **Testing & Quality Engineering:** Pirámide de pruebas (Unitarias, Integración, API) e inclusión dentro del pipeline de CI/CD.
- **Security Engineering:** Threat Modeling, prevención de vulnerabilidades del OWASP Top 10 y gestión de secretos.
- **Performance & Observabilidad:** Trazabilidad distribuida con `Correlation IDs`, métricas, structured logging y health checks.

### ⚡ Fase 8: Domain-Driven Design & Event-Driven Architecture (`v2.0`)
- **Strategic DDD:** Mapeo de subdominios, Ubiquitous Language y delimitación de *Bounded Contexts* (`Identity`, `Customers`, `Accounts`, `Transactions`, `Transfers`, `Notifications`).
- **Modular Monolith & Event-Driven:** Aislamiento modular del monolito y publicación de eventos de integración asíncronos mediante RabbitMQ/Message Broker.
- **Sistemas Distribuidos:** Manejo de resiliencia, retries, idempotencia, Dead Letter Queues (DLQ) y consistencia eventual.

### 🌐 Fase 9: Global System Design & Enterprise Architecture (`v3.0`)
- **Global System Design:** Definición de *Architecture Drivers*, atributos de calidad y diagramado C4 para operar a nivel internacional.
- **Vertical Slice Functional:** Implementación completa de un nuevo requerimiento empresarial crítico atravesando todas las capas del sistema.
- **Defensa de Arquitectura:** Documentación técnica integral de las decisiones de diseño, trade-offs y riesgos asumidos en la plataforma.

---

## 🔐 Matriz de Seguridad y Roles Proyectada

| Rol | Permisos y Alcance de Operación |
| :--- | :--- |
| **`CUSTOMER`** | Consulta de saldo propio, historial de movimientos, transferencias y pagos. |
| **`EMPLOYEE`** | Gestión operativa de solicitudes, verificación de clientes y soporte administrativo. |
| **`ADMINISTRATOR`** | Configuración de límites globales del banco, auditoría de logs y gestión de usuarios. |
| **`AUDITOR`** | Acceso en modo lectura a reportes financieros y trazabilidad transaccional. |

---

## 🏛️ Decisiones Arquitectónicas Propuestas (ADR Summary)

- **ADR-001 (Adopción de Identidad y Visión):** Selección de la identidad nórdica *Valhalla Vault* y estructura de ramas por hitos para respaldar el portafolio profesional.
- **ADR-002 (Monolito Modular vs. Microservicios):** Adopción inicial de un *Modular Monolith* para resguardar la consistencia transaccional del Banking Core, aislando únicamente servicios asíncronos de alta carga como Notificaciones.
- **ADR-003 (Clean & Hexagonal Architecture):** Aislamiento del dominio financiero respecto a Spring Boot y tecnologías externas mediante *Ports & Adapters*.
- **ADR-004 (Event-Driven Architecture & Consistencia Eventual):** Procesamiento de tareas secundarias (auditoría y notificaciones) mediante eventos de integración asíncronos con RabbitMQ.

---
*Proyecto de ingeniería de mi portafolio personal enfocado en demostrar capacidades de diseño y desarrollo de software End-to-End.*