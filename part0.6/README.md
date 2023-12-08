sequenceDiagram
    participant browser
    participant server

    Comment: With the page already loaded with the respective GET methods (as in the previous exercise).

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Status Code 201 Created
    deactivate server

    Comment: This way it does not return a redirect to a GET method, and it is not necessary
     to make the requests again because the page is not reloaded. But the data has been updated.