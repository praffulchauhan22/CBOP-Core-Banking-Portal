# CBOP – System Architecture

```mermaid
flowchart LR
    UI[CBOP.Web<br/>Razor UI]
    API[CBOP.API<br/>REST APIs]
    APP[Application Layer]
    DOM[Domain Layer]
    INFRA[Infrastructure Layer]
    DB[(Oracle Database)]
    AD[Active Directory / SSO]

    UI --> API
    API --> APP
    APP --> DOM
    APP --> INFRA
    INFRA --> DB
    INFRA --> AD
