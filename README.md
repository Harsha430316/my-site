```mermaid
graph TD
    A[Start] --> B[Input Columns & Language Preference]
    B --> C[Perform SQL Search with Original Columns (English)]
    B --> D[Translate Columns using LLM (if not English)]
    D --> E[Perform SQL Search with Translated Columns]
    C --> F[Get Top 5 Results (English)]
    E --> G[Get Top 5 Results (Translated)]
    F --> H[Combine Top 10 Results]
    G --> H
    H --> I[Use LLM as Judge to Select Best Match]
    I --> J[Final Result]
```
