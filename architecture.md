```mermaid
graph TD
    subgraph Users
        direction LR
        Learner["User (Learner)"]
    end

    subgraph "Math Booster System"
        direction LR
        App["App (Math Booster)"]
        WebApp["Web Application"]
        MobileApp["Mobile Application"]
        API["API"]
        Database["MongoDB Database"]
        AI["AI Service (Real-Time Chat)"]
        Analysis["Analysis (Performance & Recommendations)"]
    end

    Learner -->|Registers/Logs In| WebApp
    Learner -->|Registers/Logs In| MobileApp
    WebApp --> API
    MobileApp --> API
    API --> Database
    API --> AI
    AI -->|Provides Chat Interface| App
    Database -->|Stores User Data & Math Content| API
    API -->|Safeguards Data & System| Database
    Analysis -->|Generates Reports & Recommendations| API
    Database -->|Stores Reports| Analysis
    AI -->|Outsourced AI Service| API

