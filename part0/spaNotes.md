::: mermaid
sequenceDiagram
participant User
participant Browser
participant SPA
participant Server

    User->>Browser: Open SPA URL
    Browser->>Server: Request initial HTML/JS/CSS
    Server-->>Browser: Return initial HTML/JS/CSS
    Browser->>SPA: Load and execute initial JavaScript
    SPA->>SPA: Initialize app state and components

    User->>SPA: Enter note text
    SPA->>SPA: Store note text in state

    User->>SPA: Click "Save" button
    SPA->>Browser: Show loading indicator (optional)
    SPA->>Server: Send POST request with note data
    Server->>Server: Process request and save note
    Server-->>SPA: Return success response
    SPA->>SPA: Update app state with new note
    SPA->>Browser: Update DOM with new note
    Browser->>User: Display new note

:::
