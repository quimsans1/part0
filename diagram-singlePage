sequenceDiagram
    participant browser
    participant server

    Note right of browser: The user writes a new note and presses "Save"

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    Note right of server: The server recives the new note and saves it in the data base
    server-->>browser: Confirmation in JSON format
    deactivate server

    Note right of browser: The browser updates the list of notes without refreshing the page

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: JSON with the updated list of notes
    deactivate server

    Note right of browser: The browser renders the new note on the list dynamically
