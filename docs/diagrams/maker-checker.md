# Maker–Checker Transaction Workflow

```mermaid
flowchart LR
    Teller --> Initiate[Initiate Transaction]
    Initiate --> Pending[Pending Approval]
    Pending -->|Approve| Approved
    Pending -->|Reject| Rejected
    Approved --> Post[Post to Account]
