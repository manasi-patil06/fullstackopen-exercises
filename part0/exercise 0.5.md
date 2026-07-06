```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Opens the app
    Browser->>Server: Get HTML page
    Server-->>Browser: HTML page

    Browser->>Server: Get CSS file
    Server-->>Browser: CSS file

    Browser->>Server: Get JavaScript file
    Server-->>Browser: JavaScript file

    Browser->>Server: Get notes data
    Server-->>Browser: JSON notes

    Note right of Browser: Browser displays notes
```
