# Sample Mermaid Charts

This document contains various examples of Mermaid charts that can be rendered in Markdown.

## 1. Flowchart Example

```mermaid
flowchart TD
    A[Start] --> B{Is it working?}
    B -->|Yes| C[Great!]
    B -->|No| D[Debug]
    D --> E[Fix the bug]
    E --> B
    C --> F[Deploy]
    F --> G[End]
```

## 2. Sequence Diagram Example

```mermaid
sequenceDiagram
    participant User
    participant Frontend
    participant Backend
    participant Database
    
    User->>Frontend: Click button
    Frontend->>Backend: API request
    Backend->>Database: Query data
    Database-->>Backend: Return data
    Backend-->>Frontend: JSON response
    Frontend-->>User: Update UI
```

## 3. Class Diagram Example

```mermaid
classDiagram
    class Animal {
        +String name
        +int age
        +makeSound()
    }
    
    class Dog {
        +String breed
        +bark()
    }
    
    class Cat {
        +String color
        +meow()
    }
    
    Animal <|-- Dog
    Animal <|-- Cat
```

## 4. Gantt Chart Example

```mermaid
gantt
    title Project Timeline
    dateFormat  YYYY-MM-DD
    section Planning
    Requirements Gathering    :done, req1, 2024-01-01, 2024-01-07
    Design Phase             :active, design, 2024-01-08, 2024-01-21
    section Development
    Frontend Development     :dev1, 2024-01-22, 2024-02-15
    Backend Development      :dev2, 2024-01-22, 2024-02-15
    section Testing
    Unit Testing             :test1, 2024-02-16, 2024-02-25
    Integration Testing      :test2, 2024-02-26, 2024-03-05
```

## 5. Pie Chart Example

```mermaid
pie title Programming Languages Used
    "JavaScript" : 35
    "Python" : 25
    "Java" : 20
    "C++" : 10
    "Other" : 10
```

## 6. State Diagram Example

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Processing : Start
    Processing --> Success : Complete
    Processing --> Error : Fail
    Success --> [*]
    Error --> Idle : Retry
```

## 7. Entity Relationship Diagram Example

```mermaid
erDiagram
    USER ||--o{ ORDER : places
    USER {
        string name
        string email
        string password
    }
    ORDER ||--|{ ORDER_ITEM : contains
    ORDER {
        int id
        date created_at
        string status
    }
    ORDER_ITEM {
        int quantity
        float price
    }
    PRODUCT ||--o{ ORDER_ITEM : includes
    PRODUCT {
        string name
        string description
        float price
    }
```

## 8. Mind Map Example

```mermaid
mindmap
  root((Web Development))
    Frontend
      HTML
      CSS
      JavaScript
        React
        Vue
        Angular
    Backend
      Node.js
      Python
        Django
        Flask
      Java
        Spring
    Database
      SQL
        MySQL
        PostgreSQL
      NoSQL
        MongoDB
        Redis
```

## 9. Git Graph Example

```mermaid
gitgraph
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
```

## 10. User Journey Example

```mermaid
journey
    title User Journey
    section Discovery
      Visit Website: 5: User
      Browse Products: 4: User
    section Purchase
      Add to Cart: 3: User
      Checkout: 2: User
      Payment: 1: User
    section Post-Purchase
      Receive Email: 5: User
      Track Order: 4: User
      Leave Review: 3: User
```

---

## Notes

- Mermaid charts are rendered automatically in many Markdown viewers including GitHub, GitLab, and many documentation platforms
- The syntax is quite intuitive and similar to other diagramming tools
- You can customize colors, styles, and layouts using Mermaid's configuration options
- These charts are great for documentation, technical specifications, and project planning
