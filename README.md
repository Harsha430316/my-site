```mermaid
graph TD
    A[Start] --> B[Input Columns and Language];
    B --> C{Is Language English?};
    C -- Yes --> D[SQL Search Original Columns];
    C -- No --> E[Translate Columns using LLM];
    E --> F[SQL Search Translated Columns];
    D --> G[Get Top 5 Original Query];
    F --> H[Get Top 5 Translated Query];
    G --> Judge1[LLM Judge (5 Original Results)];
    H --> Judge2[LLM Judge (5 Translated Results)];
    Judge1 --> K[Combine Results];
    Judge2 --> K;
    K --> JudgeCombined[LLM Judge (Combined Results)];
    JudgeCombined --> M[Final Result];
```
