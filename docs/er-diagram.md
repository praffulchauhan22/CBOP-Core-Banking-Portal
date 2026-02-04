# ER Diagram – Core Banking (Oracle)

```mermaid
erDiagram
    USERS {
        number USER_ID PK
        varchar USERNAME
        varchar PASSWORD_HASH
        varchar EMAIL
        varchar STATUS
        date CREATED_ON
    }

    ROLES {
        number ROLE_ID PK
        varchar ROLE_NAME
    }

    USER_ROLES {
        number USER_ID FK
        number ROLE_ID FK
    }

    CUSTOMERS {
        number CUSTOMER_ID PK
        varchar FULL_NAME
        varchar PAN_ENCRYPTED
        varchar AADHAAR_ENCRYPTED
        date CREATED_ON
    }

    ACCOUNTS {
        number ACCOUNT_ID PK
        number CUSTOMER_ID FK
        varchar ACCOUNT_NUMBER_ENC
        varchar ACCOUNT_TYPE
        number BALANCE
        varchar STATUS
    }

    TRANSACTIONS {
        number TRANSACTION_ID PK
        number ACCOUNT_ID FK
        number AMOUNT
        varchar TRANSACTION_TYPE
        varchar STATUS
        date CREATED_ON
    }

    AUDIT_LOG {
        number AUDIT_ID PK
        number USER_ID
        varchar ACTION
        varchar ENTITY
        date ACTION_TIME
    }

    USERS ||--o{ USER_ROLES : assigned
    ROLES ||--o{ USER_ROLES : mapped
    CUSTOMERS ||--o{ ACCOUNTS : owns
    ACCOUNTS ||--o{ TRANSACTIONS : records
    USERS ||--o{ AUDIT_LOG : generates
