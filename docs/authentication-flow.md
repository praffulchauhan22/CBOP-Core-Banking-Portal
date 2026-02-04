# Authentication & Authorization Flow

```mermaid
flowchart TD
    User --> Login[Login Screen]
    Login -->|SSO Enabled| AD[Active Directory]
    Login -->|Local Login| Identity[ASP.NET Identity]
    AD --> Claims[Claims Principal]
    Identity --> Claims
    Claims --> Dashboard
