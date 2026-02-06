
# design-doc.md

## Tech Stack

* Game engine: Unity (2D)
* Programmeertaal: C#
* Versiebeheer: Git + GitHub
* Grafische assets: Aseprite / OpenGameArt
* Audio: Bfxr / freesound.org
* Ontwikkelomgeving: Visual Studio / VS Code
* Platform: PC (Windows)

## Globale Architectuur

### Overzicht

Het spel is opgebouwd volgens een modulaire structuur met gescheiden systemen voor gameplay, UI en data-opslag.

### Componenten

* Player System: Beweging, schieten, health
* Enemy System: AI, spawning, gedrag
* Boss System: Speciale patronen en aanvallen
* Skill Tree System: Upgrades en statistieken
* Score System: Puntentelling en opslag
* UI System: Menu’s, HUD, upgrade-scherm

### Datastroom

1. Speler start level
2. Enemy Spawner genereert vijanden
3. Player en vijanden interacteren
4. Score wordt bijgewerkt
5. Skillpunten worden opgeslagen
6. Volgend level wordt geladen

## Belangrijke Keuzes

* Keuze voor Unity vanwege snelle 2D-ontwikkeling
* Gebruik van ScriptableObjects voor upgrades
* Singleplayer-only om scope klein te houden
* Simpele pixel-art stijl voor snelle productie
* Lokale opslag voor progressie (geen server)

## Bekende Risico’s

* Tijdgebrek bij implementatie van skill tree
* Balanceren van moeilijkheidsgraad
* Bugs in collision-detectie
* Prestatieproblemen bij veel vijanden
* Onvoldoende playtesting

## Mitigatie

* Begin met een simpele skill tree (3–5 upgrades)
* Test elk level apart
* Regelmatig commits maken
* Basis performance testing
* Feedback vragen aan klasgenoten
