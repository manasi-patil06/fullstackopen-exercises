```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Type a note
    User->>Browser: Press Save

    Browser->>Server: Send note to server
    Server-->>Browser: Note stored

    Note right of Browser: Browser shows the new note without refreshing
```
