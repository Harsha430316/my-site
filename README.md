```mermaid
graph LR
    A[Input: Columns & Target Language] --> B{SQL Search (English)};
    A --> C{Translate Columns to Target Language};
    C --> D{SQL Search (Target Language)};
    B --> E[Top 5 Results (English)];
    D --> F[Top 5 Results (Target Language)];
    E --> G{LLM Judge: Compare & Rank};
    F --> G;
    G --> H[Output: Best Match];
```
