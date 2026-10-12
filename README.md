# ᚠ VALHALLA VAULT - Digital Banking Platform
> **Enterprise Banking Core y Secure Financial Architecture**


<p align="center">
  <img src="./assets/images/logo.png" alt="Valhalla Vault Logo" width="250">
</p>

## 📌 Nota sobre el Proyecto
**Valhalla Vault** es un proyecto ficticio en desarrollo, concebido exclusivamente con fines educativos y de aprendizaje personal para mi portafolio profesional. El nombre y la identidad visual están inspirados en la **mitología nórdica**, representando la fortaleza, la custodia de activos y la protección inexpugnable de una bóveda financiera.

> ⚠️ **Nota de evolución:** Este `README.md` es un documento dinámico que se irá actualizando a medida que el proyecto avance y se completen las distintas etapas. Toda la documentación detallada, diagramas de arquitectura y decisiones de diseño se irán almacenando progresivamente en la carpeta `/docs`.

---

## 🏛️ Visión Técnica
La plataforma está proyectada como un sistema bancario digital *Fullstack* evolutivo. Su propósito es simular un núcleo transaccional real diseñado para escalar progresivamente desde un prototipo local hasta una arquitectura empresarial distribuida basada en microservicios, comunicación asíncrona por eventos y principios de *Clean y Hexagonal Architecture*.

---

## 🌿 Estrategia de Ramas (Git Branching Strategy)
Para mantener un historial de desarrollo limpio y organizado, **cada avance del roadmap se desarrollará en su propia rama (*branch*)**.

- `main`: Contendrá la versión estable e integrada del sistema.
- `feature/m1-banking-core`: Implementación proyectada del modelo de dominio y reglas financieras básicas en consola.
- `feature/m2-spring-backend`: Desarrollo planeado de la base de datos relacional, APIs REST y seguridad JWT.
- `feature/m3-angular-experience`: Construcción de la interfaz web interactiva y cliente SPA.
- `feature/m4-clean-architecture`: Refactorización hacia Ports y Adapters y dockerización del entorno.
- `feature/m5-ai-hardening`: Optimización asistida por IA, pirámide de pruebas y controles de seguridad.
- `feature/m6-ddd-event-driven`: Modelado de Bounded Contexts y mensajería asíncrona.

---

## 🛠️ Tech Stack Principal

- **Backend Core:** Java 17+, Spring Boot (Spring Web, Spring Data JPA, Spring Security).
- **Servicios Complementarios:** Node.js, TypeScript (Notification Service).
- **Frontend Experience:** Angular 17+, TypeScript, HTML5, CSS3/SASS.
- **Base de Datos y Persistencia:** PostgreSQL, Hibernate / JPA, SQL DDL/DML.
- **Seguridad y Autenticación:** JWT (JSON Web Tokens), BCrypt Hashing, RBAC (Role-Based Access Control).
- **Infraestructura y DevOps:** Docker, Docker Compose, GitHub Actions (CI/CD), OpenAPI / Swagger.
- **Arquitectura y Patrones:** Domain-Driven Design (DDD), Clean Architecture, Ports y Adapters, Event-Driven Architecture (RabbitMQ/Message Broker).

---

## 🗺️ Mapa de Evolución de la Plataforma (Roadmap Proyectado)

### 🟢 Módulo 1: Valhalla Core — Foundations y POO (`v0.1`)
- **Modelado del Dominio Financiero:** Abstracción y encapsulamiento de entidades (`Customer`, `Account`, `Transaction`).
- **Reglas Financieras Básicas:** Validación de saldos, control de límites operativos y cálculo de comisiones.
- **Consola Transaccional:** Registro e historial de depósitos, retiros y transferencias con manejo estructurado de excepciones.

### 🟡 Módulo 2: Secure Banking Backend y APIs (`v0.4`)
- **Persistencia Relacional:** Diseño del modelo Entidad-Relación en PostgreSQL con integridad referencial y soporte ACID.
- **REST APIs:** Desarrollo de controladores en Spring Boot para las operaciones del banco.
- **Seguridad JWT:** Configuración de filtros con Spring Security, cifrado de credenciales y autorización por roles (`CUSTOMER`, `EMPLOYEE`, `ADMINISTRATOR`).
- **Microservicio de Notificaciones:** Integración progresiva con un servicio secundario en Node.js y TypeScript.

### 🔵 Módulo 3: Valhalla Banking Experience — Frontend (`v0.6`)
- **Estructura Web y Responsive Design:** Creación de un Dashboard interactivo adaptado a dispositivos móviles y escritorio.
- **Single Page Application (Angular):** Desarrollo de componentes reactivos, consumo de servicios con RxJS, `Guards` de navegación e `Interceptors` para el token JWT.
- **Flujos Integrados:** Autenticación, consulta de extractos, registro de beneficiarios y envío de dinero.

### 🔴 Módulo 4 y 5: Clean Architecture y Fullstack Integration (`v1.0`)
- **Inversión de Dependencias:** Refactorización progresiva hacia *Ports y Adapters* (Arquitectura Hexagonal) y aplicación de principios SOLID.
- **Contratos Abiertos:** Documentación interactiva de endpoints mediante OpenAPI / Swagger.
- **Automatización y Contenedores:** Orquestación del backend, frontend, servicios y base de datos mediante `Docker Compose`.

### 🟣 Módulo 6 y 7: AI-Assisted Engineering y Hardening (`v1.2`)
- **Desarrollo Aumentado:** Optimización, análisis de cobertura y debugging asistido por Inteligencia Artificial (Cursor AI).
- **Pruebas Automatizadas:** Implementación de la pirámide de testing (Unitarias, Integración, APIs) y controles OWASP para la mitigación de vulnerabilidades.
- **Observabilidad:** Integración de métricas de rendimiento, structured logging y trazabilidad distribuida mediante `Correlation IDs`.

### ⚡ Módulo 8 y 9: Scalable Banking Architecture y DDD (`v3.0`)
- **Strategic DDD:** Mapeo de subdominios y delimitación de *Bounded Contexts* (`Identity`, `Accounts`, `Transactions`, `Transfers`, `Notifications`).
- **Event-Driven Architecture:** Publicación e integración de eventos asíncronos mediante *Message Broker* (RabbitMQ).
- **Gobierno Arquitectónico:** Documentación técnica estandarizada mediante *Architecture Decision Records* (ADRs) y diagramas C4 en la carpeta `/docs`.

---

## 🔐 Matriz de Seguridad y Roles Proyectada

| Rol | Permisos y Alcance de Operación |
| :--- | :--- |
| **`CUSTOMER`** | Consulta de saldo propio, historial de movimientos, transferencias y pagos. |
| **`EMPLOYEE`** | Gestión operativa de solicitudes, verificación de clientes y soporte. |
| **`ADMINISTRATOR`** | Configuración de límites globales del banco, auditoría de logs y gestión de usuarios. |
| **`AUDITOR`** | Acceso en modo lectura a reportes financieros y trazabilidad transaccional. |

---

## 🏛️ Decisiones Arquitectónicas Propuestas (ADR Summary)

* **ADR-001 (Monolito Modular vs. Microservicios):** Se contempla un *Modular Monolith* inicialmente para resguardar la consistencia transaccional del Banking Core, proyectando el aislamiento únicamente de servicios asíncronos de alta carga como Notificaciones.
* **ADR-002 (Clean Architecture):** Las reglas de negocio y entidades financieras del dominio se diseñarán independientes del framework Spring Boot, protegiendo la lógica del banco ante cambios tecnológicos.
* **ADR-003 (Eventual Consistency):** Las operaciones de auditoría y notificaciones secundarias se planificarán para procesarse de manera asíncrona mediante eventos de integración, optimizando el tiempo de respuesta del endpoint de transferencias.

---
*Proyecto educativo de mi portafolio personal enfocado en demostrar capacidades de Ingeniería de Software End-to-End.*
