Sequence diagram for Exercise 0.6 follows

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: Upon pressing the save button, the page appends the note to the end of the list of notes, redraws the list of notes on the webpage, then sends a POST to the server.

    browser->>server: POST [content: textboxContent, date: currentDateTime] https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: message: "note created"
    deactivate server

    Note right of browser: The browser sends the contents of the textbox as a string and the date/time to the server in JSON format
    
```