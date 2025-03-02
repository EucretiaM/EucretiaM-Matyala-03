```mermaid
graph TD
    subgraph Users
        Learner["User (Learner)"]
    end

    subgraph "Math Booster System"
        App["App (Math Booster)"]
        WebApp["Web Application"]
        MobileApp["Mobile Application"]
        API["API"]
        Database["MongoDB Database"]
        AI["AI Service"]
    end

    Learner -->|Registers/Logs In| WebApp
    Learner -->|Registers/Logs In| MobileApp
    WebApp --> API
    MobileApp --> API
    API --> Database
    API --> AI
    AI -->|Provides Recommendations| App
    Database -->|Stores Data| API
