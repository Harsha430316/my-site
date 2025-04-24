```mermaid
graph TD
    A[Start] --> B[Input Columns and Language]
    B --> C{Is Language English?}
    C -- Yes --> D[SQL Search using Original Columns]
    C -- No --> E[Translate Columns using LLM]
    E --> F[SQL Search using Translated Columns]
    D --> G[Get Top 5 Results from Original Query]
    F --> H[Get Top 5 Results from Translated Query]
    G --> I[LLM Judge (5 Results)]
    H --> J[LLM Judge (5 Results)]
    I --> K[Combine Results]
    J --> K
    K --> L[LLM Judge (Combined Results)]
    L --> M[Final Result]
```
