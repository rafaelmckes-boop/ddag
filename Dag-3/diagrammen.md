# Diagrammen – Hollowcaster Bossfight

## Applicatie-overzicht

```mermaid
graph TD
    Player --> UI
    Player --> Arena
    Player --> BossController
    BossController --> HealthSystem
    BossController --> AttackSystem
    HealthSystem --> UI
    SoundSystem --> Player
    Arena --> Player
```

---

## Datastroom / API-flow

```mermaid
sequenceDiagram
    participant Player
    participant Client
    participant Server
    participant Boss
    participant UI

    Player->>Client: Aanval uitvoeren
    Client->>Server: Stuur aanval data
    Server->>Boss: Bereken schade
    Boss->>Server: Update health
    Server->>UI: Update healthbar
    Server->>Client: Stuur resultaat
    Client->>Player: Toon feedback
```

---

## Prompt 6 – Diagrammen maken met Mermaid

"Maak twee Mermaid-diagrammen voor een Roblox bossfight-project: één applicatie-overzicht en één datastroom/sequence diagram. Gebruik duidelijke componentnamen."
