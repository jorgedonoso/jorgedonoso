# Summer 2026 Update

Open to full stack IC or contract opportunities.

## Current Project: AI Japanese Learning Tool
Building a full-stack SaaS that turns user-uploaded images into Japanese learning content using LLM APIs.

**Status:** Live in production. Demo available on request.

## Core Overview

```mermaid
flowchart TD
   A([Start Project]) --> B[Upload Image]

    B --> C[OCR Processing]

    C --> D{Japanese Detected?}
    D -->|Yes| E[LLM Processing]
    D -->|No| B[Upload Image]

    E --> F[(Database)]
    F --> G[Project View]

    G --> H[Generate Deep Dive]
    G --> I[Generate Example Sentences]

    H --> J[LLM Processing]
    I --> J

    J --> K[(Database)]
    K --> G

    %% Token system
    B -. Consume Tokens .-> T[(Token System)]
    H -. Consume Tokens .-> T
    I -. Consume Tokens .-> T

    %% Errors
    C -->|OCR Error| X[Error State]
    E -->|LLM Error| X
    J -->|LLM Error| X
    X --> G

    %% Styling
    classDef token fill:#E8F5E9,stroke:#43A047,color:#1B5E20;
    classDef llm fill:#FFF3E0,stroke:#FB8C00,color:#E65100;
    classDef error fill:#FFEBEE,stroke:#E53935,color:#B71C1C;
    classDef db fill:#E3F2FD,stroke:#1E88E5,color:#0D47A1;

    class C,E,J llm;
    class T token;
    class X error;
    class F,K db;
```
