# Reporting & Export Flow

```mermaid
flowchart LR
    User --> Filters[Select Filters]
    Filters --> Query[Optimized Queries]
    Query --> Report[Generate Report]
    Report --> PDF[PDF Export]
    Report --> Excel[Excel Export]
