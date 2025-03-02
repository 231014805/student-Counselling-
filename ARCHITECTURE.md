```mermaid
flowchart TD
    A[Student searches for available slots] -->|View available slots| B[Slot Selection]
    B --> C{Is the selected slot available?}
    C -->|Yes| D[Book Slot]
    C -->|No| E[Show alternative slots]
    D --> F[Send Confirmation Email to Student]
    D --> G[Send Confirmation Email to Counselor]
    F --> H[Student receives appointment reminder]
    G --> I[Counselor receives appointment reminder]
