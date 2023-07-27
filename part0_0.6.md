````mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: STATUS 201 CREATED
    deactivate server
    Note right of browser: The new note as JSON data containing both the content of the note (content) and the timestamp (date). <br> Use the JavaScript code it fetched from the server to send the form data to the server
````