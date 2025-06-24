
# BookBuddy – Lern- & Übungsprojekt mit Angular 17+

Verwalte deine private Bibliothek – und lerne dabei Schritt für Schritt **Angular-Grundlagen, Services, Forms, Routing, Signals** sowie einen Hauch **Unit-Testing**.  
Dieses README führt dich von der Installation bis zum Test-Run.

---

## Inhaltsverzeichnis
1. [Lernziele](#lernziele)
2. [Quick Start](#quick-start)
3. [User-Stories & Aufgaben](#user-stories--aufgaben)
4. [Projektstruktur](#projektstruktur)
5. [Verfügbare NPM-Scripts](#verfügbare-npm-scripts)
6. [Tests](#tests)
7. [Hilfestellung](#hilfestellung)
8. [Lizenz](#lizenz)

---

## Lernziele

| Thema                | Du lernst …                                  |
|----------------------|----------------------------------------------|
| **Angular Intro**    | Projekt erzeugen, Module & Komponenten       |
| **Services**         | Dependency Injection, Datenkapselung         |
| **Forms**            | Template- & Reactive Forms, Validierung       |
| **Routing**          | Grundrouting, Parameter, (optionale Guards)  |
| **Signals**          | Reaktiver State ohne Drittbibliothek         |
| **Unit-Tests**       | Zwei kleine, praxisnahe Tests                |

---

## Quick Start

```bash
# 1 Projekt anlegen
npx @angular/cli new book-buddy --routing --style=scss
cd book-buddy

# 2 Abhängigkeiten installieren
npm install

# 3 Dev-Server starten
npm start       # Alias für: ng serve -o
