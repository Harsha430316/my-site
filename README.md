```mermaid
graph TD
    A[Start] --> B[Input: Columns title, episode title, description & Language];
    B --> C{Is Language English?};

    C -- Yes --> D[Build & Run SQL Query Original Columns];
    D --> E[Get Top 5 Results Original Query];
    E --> F[LLM Judges the 5 Original Results];

    C -- No --> G[Translate Columns to English using LLM];
    G --> H[Build & Run SQL Query Translated Columns];
    G --> I[Build & Run SQL Query Original Columns]; 
    H --> J[Get Top 5 Results Translated Query];
    I --> K[Get Top 5 Results Original Query];
    J --> L[Combine Results 10 Total];
    K --> L;
    L --> M[LLM Judges the 10 Combined Results];

    F --> N[Final Result Selected by LLM];
    M --> N;```
