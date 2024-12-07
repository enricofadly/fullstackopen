:::mermaid
sequenceDiagram
participant Browser
participant SPA
participant Server

    Browser->>Server: Request initial HTML/JS/CSS
    Server-->>Browser: Return initial HTML/JS/CSS
    Browser->>SPA: Load and execute initial JavaScript
    SPA->>SPA: Initialize app state and components
    SPA-->>Browser: Return the HTML/JS/CSS

:::
