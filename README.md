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

| Thema             | Du lernst …                                 |
| ----------------- | ------------------------------------------- |
| **Angular Intro** | Projekt erzeugen, Module & Komponenten      |
| **Services**      | Dependency Injection, Datenkapselung        |
| **Forms**         | Template- & Reactive Forms, Validierung     |
| **Routing**       | Grundrouting, Parameter, (optionale Guards) |
| **Signals**       | Reaktiver State ohne Drittbibliothek        |
| **Unit-Tests**    | Zwei kleine, praxisnahe Tests               |

---

## Quick Start

```bash
# 1 Projekt anlegen
npx @angular/cli new book-buddy --routing --style=scss
cd book-buddy

# 2 Abhängigkeiten installieren
npm install

# 3 Dev-Server starten
npm start       # Alias für: ng serve -o
```

> **Zeitaufwand Setup:** ≈ 15 Minuten

---

## User-Stories & Aufgaben

1. **Projektinitialisierung**
   *Als Entwickler* möchte ich mit `ng new book-buddy --routing --style=scss` ein neues Angular‑Projekt anlegen und es im Browser starten, **damit** ich eine funktionierende Basis für die weitere Entwicklung habe.
   **Kernkonzepte:** Angular Intro

2. **BookService & Signals**
   *Als Benutzer* möchte ich, dass alle Buchdaten in einem `BookService` verwaltet werden, der seinen Zustand als `signal<Book[]>` bereitstellt und CRUD‑Methoden (`addBook`, `updateBook`, `deleteBook`, `getBookById`) anbietet, **damit** jede Komponente dieselben, sofort aktualisierten Daten erhält.
   **Kernkonzepte:** Services, Signals

3. **Bücherliste**
   *Als Leser* möchte ich in einem `BookListComponent` eine Tabelle aller Bücher sehen und per Klick auf eine Zeile zur Detailansicht (`/books/:id`) navigieren, **damit** ich schnell Details ansehen kann.
   **Kernkonzepte:** Components, Routing

4. **Detailansicht**
   *Als Leser* möchte ich in der `BookDetailComponent` alle Infos zu einem Buch sehen, die via Routen‑Parameter geladen werden, **damit** ich dessen Daten überprüfen oder bearbeiten kann.
   **Kernkonzepte:** Routing, Signals

5. **Neues Buch anlegen**
   *Als Leser* möchte ich unter `/books/new` ein **Reactive Form** ausfüllen können, um ein neues Buch hinzuzufügen; das Formular soll Pflichtfelder validieren und mich erst speichern lassen, wenn alles korrekt ist.
   **Kernkonzepte:** Reactive Forms

6. **Buch bearbeiten**
   *Als Leser* möchte ich in der Detailansicht einen „Bearbeiten“-Button haben, der mich zu `/books/:id/edit` führt, wo dasselbe Formular mit bestehenden Daten vorbefüllt ist, **damit** ich Einträge bequem aktualisieren kann.
   **Kernkonzepte:** Routing, Forms

7. **Suche & Filter**
   *Als Leser* möchte ich oberhalb der Liste ein Suchfeld (Template‑Driven Form) haben, das die Bücherliste live filtert, **damit** ich Titel schneller finde.
   **Kernkonzepte:** Template Forms, Signals

8. **Lesestatus‑Badge**
   *Als Leser* möchte ich in der Toolbar jederzeit eine Badge sehen („Gelesen X / Gesamt Y“), die sich automatisch aktualisiert, **damit** ich meinen Lesefortschritt auf einen Blick habe.
   **Kernkonzepte:** Signals

9. **Unit‑Tests**
   *Als Entwickler* möchte ich zwei Unit‑Tests definieren – einen für `BookService.addBook()` und einen für die Anzeige der Buchanzahl im `BookListComponent` – **damit** ich die Kernlogik automatisch verifizieren kann.
   **Kernkonzepte:** Unit‑Testing

**Optional‑Erweiterungen**

* Persistenz via `localStorage`.
* Route Guard für ungültige Buch‑IDs.
* Mini‑Progress‑Bar (gelesene Seiten).

---

## Projektstruktur

```
book-buddy/
├── src/
│   ├── app/
│   │   ├── core/            # Globale Services, Guards
│   │   ├── features/
│   │   │   └── books/       # Book-Domain (Components, Service, Models)
│   │   └── shared/          # Wiederverwendbare UI-Bausteine
│   └── assets/
└── README.md
```

---

## Verfügbare NPM-Scripts

| Befehl             | Zweck                                         |
| ------------------ | --------------------------------------------- |
| `npm start`        | Dev-Server + Live-Reload (`ng serve`)         |
| `npm run build`    | Production-Build (`ng build`)                 |
| `npm test`         | Unit-Tests einmalig (`ng test --watch=false`) |
| `npm run lint`     | ESLint-Prüfung                                |
| `npm run prettier` | Code-Formatierung                             |

---

## Tests

Die Übung umfasst **nur zwei** Unit‑Tests, um Tests kennenzulernen, ohne dich zu überfordern:

1. **Service-Test** – prüft, ob `addBook()` ein Buch ans Array anhängt.
2. **Component-Test** – verifiziert, dass `BookListComponent` die Anzahl der Bücher korrekt rendert.

```bash
# Tests ausführen
npm test
```

---

