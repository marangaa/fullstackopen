# Creating a New Note - Single Page App

sequenceDiagram
    participant browser
    participant server

    Note right of browser: User writes note and clicks Save button
    Note right of browser: Browser adds new note to notes list<br/>and redraws notes using DOM-API
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note left of server: Server processes the new note
    server-->>browser: Response: {"message":"note created"}
    deactivate server

    Note right of browser: Browser stays on same page,<br/>no additional HTTP requests needed