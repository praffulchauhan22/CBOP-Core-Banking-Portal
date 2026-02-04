# API Sequence – Transaction Processing

```mermaid
sequenceDiagram
    participant UI as Web UI
    participant API as Transaction API
    participant APP as Application Layer
    participant DB as Oracle DB
    participant AUDIT as Audit Service

    UI->>API: POST /api/transactions
    API->>APP: Validate request
    APP->>DB: Check account balance
    DB-->>APP: Balance OK
    APP->>DB: Insert transaction (Pending)
    APP->>AUDIT: Log action
    APP-->>API: Transaction Pending Approval
    API-->>UI: Success response
