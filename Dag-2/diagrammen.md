sequenceDiagram
    participant App as Bibliotheek App
    participant API as REST API
    participant DB as Database

    App->>API: GET /boeken
    API->>DB: Query boeken
    DB-->>API: Boekenlijst
    API-->>App: 200 OK + JSON

    App->>API: POST /uitleningen
    API->>DB: Nieuwe uitlening opslaan
    DB-->>API: Bevestiging
    API-->>App: 201 Created



sequenceDiagram
    participant App as Bibliotheek App
    participant API as REST API
    participant DB as Database

    App->>API: GET /boeken
    API->>DB: Query boeken
    DB-->>API: Boekenlijst
    API-->>App: 200 OK + JSON

    App->>API: POST /uitleningen
    API->>DB: Nieuwe uitlening opslaan
    DB-->>API: Bevestiging
    API-->>App: 201 Created

flowchart LR
    Gebruiker --> UC1[Boeken zoeken]
    Gebruiker --> UC2[Boek lenen]
    Gebruiker --> UC3[Boek reserveren]

    Beheerder --> UC4[Boeken toevoegen]
    Beheerder --> UC5[Leden beheren]



