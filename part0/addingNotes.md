::: mermaid
sequenceDiagram
autonumber
participant browser
participant server

    note over browser: User input the notes
    note over browser: User submitted the button
    activate server
    browser->>server: form POST data to server
    note over server: Server save the submitted<br>data to server
    server->>server: The server add the new added note
    browser->>server: The browser fetch/GET the updated html page
    server-->>browser: Server send the updated hmtl page
    deactivate server

:::
