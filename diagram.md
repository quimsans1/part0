```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/notes/new_note (sends new note data)
    activate server
    server-->>browser: Success response (note saved)
    deactivate server

    browser->>browser: Refreshes the page to display updated list of notes
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes (requests updated notes list)
    activate server
    server-->>browser: HTML document (with updated notes list)
    deactivate server
