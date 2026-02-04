# Design Document – Hollowcaster Bossfight

## Tech Stack

* **Game Engine:** Roblox Studio
* **Programmeertaal:** Lua (Roblox Lua)
* **Frameworks/Libraries:** Roblox standaard services (RunService, TweenService, DataStoreService)
* **Versiebeheer:** Roblox Studio versiegeschiedenis
* **Assets:** Roblox Toolbox en eigen modellen
* **Audio:** Roblox Sound Service

---

## Globale Architectuur

De game is opgebouwd uit verschillende scripts en onderdelen:

* **Boss Script:** Regelt AI, aanvallen en fases van de Hollowcaster
* **Health System:** Beheert de health van de boss en de speler
* **UI Script:** Toont de gezondheidsbalk en meldingen
* **Arena Script:** Beheert de omgeving en grenzen
* **Sound Script:** Regelt geluidseffecten

### Structuur

* ServerScriptService

  * BossController
  * DamageHandler
* StarterGui

  * HealthBarUI
* Workspace

  * HollowcasterModel
  * Arena
* ReplicatedStorage

  * Animations
  * Assets

---

## Belangrijke Keuzes

* Gebruik van server-side scripts voor damage en AI om cheaten te voorkomen
* Simpele AI-structuur om binnen de tijd te blijven
* Beperkt aantal aanvallen (3–4) voor overzicht
* Hergebruik van bestaande Roblox-assets waar mogelijk
* Focus op singleplayer-ervaring

---

## Bekende Risico’s

* Onverwachte bugs in AI-gedrag
* Performanceproblemen bij meerdere effecten
* Onbalans in moeilijkheidsgraad
* Tijdgebrek voor uitgebreide animaties
* Problemen met synchronisatie tussen client en server
