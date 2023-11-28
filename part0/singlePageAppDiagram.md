## 0.6: New note in Single page app diagram

### Exercise

Create a diagram depicting the situation where the user creates a new note using the single-page version of the app.

### Solution

```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    server-->>browser: Status code 201 created
    deactivate server

    Note right of browser: Server doesn't ask for a redirect, so browser stays on the same page and doesn't send any HTTP requests
```