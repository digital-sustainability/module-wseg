# Software-Engineering (WSEG)

[zum Mirror-Repository auf Github](https://github.com/digital-sustainability/module-wseg)
![GitHub](https://img.shields.io/github/license/digital-sustainability/module-wseg)

## Wichtige Links

- Moodle Kurs: <https://moodle.bfh.ch/course/view.php?id=45075>
- BigBlueButton: <https://bbb.ch-open.ch/rooms/hdh-isb-49k-ye6/join>
- BFH-GitLab Gruppe: <https://gitlab.ti.bfh.ch/w-wseg/26-hs>
  - [Wiki Page für Iterations Wrap-Ups](https://gitlab.ti.bfh.ch/groups/w-wseg/26-hs/-/wikis/home)

# Inhalte

🏗️ Hinweis: Kursinhalte in Veränderung, ggf. sind Inhalte des letzten Semesters noch verlinkt.

## Termin 0 [Vorbereitung / Setup 💻🛠️⚙️](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/00-setup/01.md) (JB)

- Entwicklungsumgebung selbständig nach [Video (13min)](https://mediaspace.bfh.ch/media/WSEG+FS26+00-Vorbereitung+++Setup+/0_kvf76d13) einrichten

### Lernziele

**Die Studierenden können ...**

- praktisch auf ihrem Arbeitsgerät Software aus unterschiedlichen Quellen via Paketmanager installieren und nach Anleitung einrichten

## Termin 1 [Einführung und Überblick 🚀](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/01-onboarding/01.md) (JB)

- Überblick Modul
- Vorstellung & Kennenlernen
- Administratives: Praxisprojekt und Prüfung
- Werkzeuge und Accounts, Terminalbasics
- Gruppenbildung und erste Projektidee

### Lernziele

- praktisch im Terminal bzw. ihrer jeweiligen Shell zwischen Ordnern wechseln und Befehle mit Parametern ausführen

## Termin 2 [Codemanagement 🗃️](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/02-codemanagement/) (MT)

- Einstieg in die Versionsverwaltung (mit git)
- Basissetup: Initialisieren und Zugriff (Clonen via SSH)
- Basisbefehle: push, pull, status, commit
- Erweiterte Befehle: branch, merge, rebase
- Kollaborationsplattform Gitlab & Modelle
- Vorstellung agiler Arbeitsweise

### Lernziele

- die Grundprinzipien und Gründe für den Einsatz einer Versionsverwaltung benennen
- Änderungen in der Versionsverwaltung einsehen und nachvollziehen
- Rituale der agilen Arbeitsweise benennen und beschreiben
- praktisch ein neues Git-Repository anlegen bzw. dieses _clonen_, sowie erste Transaktionen (Commits) vornehmen und für das Team publizieren

## Termin 3 [Frontend: Webtechnologien 🌐](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/03-web-frontend/01.md) (JB)

### Iteration 0: Pitch / Präsentation (Gitlab Projekt und Profil konfiguriert haben)

- Einstieg, Browser Dev Tools
- Entwicklungsumgebung + Übung
- HTML/CSS + Übung
- Wireframes und Design
- Arbeit am Projekt

### Lernziele

- in einfachen Worten erklären, wie eine Website erstellt werden kann und die Kommunikation mit dem Webbrowser funktioniert.
- anhand eingebauter _Developer Tools_ im Browser eine Website analysieren und damit experimentieren.
- mit Hilfe des Webstandards HTML und der Dokumentation Inhalte und Struktur einer einfachen Website gestalten.
- mit Hilfe des Webstandards CSS und der Dokumentation das Styling einer Website anpassen.
- ein Vue-Projekt (oder anderes JavaScript-Frontend) als Basis für eine _Single-Page-Application_ aufsetzen

## Termin 4 [Backend: Softwarearchitektur / Einführung Strapi ✈️ 📦](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/04-architecture-backend/01.md) (JB)

- Softwarearchitektur: Entwurf, Architekturen
- Komponenten und Bezug zu Vue
- REST APIs
- Infos Deliverable "MVP"

### Lernziele

- Den Begriff Softwarearchitektur erklären und verschiedene Architekturtypen aufzählen können
- Eine (Web-)Applikation in Komponenten zerlegen können
- Die Architektur des eigenen Projekts in einfachen Worten erklären
- Die Verwendung von REST APIs und CRUD-Operationen erläutern können
- Erstellung eines einfachen Datenmodells im Strapi-Backend

## Termin 5 [Agiles Arbeiten 🎯 / API Client verwenden](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/05-agility/) (MT)

### Lernziele

- die Prinzipien agiler Vorgehensweisen diskutieren und dafür Anwendungsmöglichkeiten im eigenen Berufsfeld erkennen (Überprüfbarkeit ? Weiter präzisieren)
- praktisch REST APIs durch einen eigenständigen API-Client testen bzw. verwenden
- praktisch das Format Markdown als Auszeichnungssprache für Dokumentationen in Gitlab verwenden
- praktisch in Git einen Branch für einen Merge-Request eröffnen und diesen nach dem _Code Review_ durch die Dozierenden selbständig zusammenführen

## Termin 6 [Strapi + Vue 🛠️ / TypeScript, OOP ⌨](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/06-api-ts/01.md) (JB)

- Anbindung Vue an Strapi
- Node.js Erläuterung
- Typescript/JavaScript
  - Typen, Objekte
  - Funktionen / this
- OOP / Klassen
- Infos Deliverable "Blog"

### Lernziele

- grundlegende Eigenschaften der Objektorientierten Programmierung (Begriffe Objekt, Instanz, Klasse, Attribut) und OOP-Konzepte (Abstraktion, Enkapsulation, Vererbung) erklären
- die Unterschiede zwischen TypeScript und JavaScript erläutern
- die Bedeutung von Node.js für den Einsatz in Web-Applikationen erläutern
- praktisch einen Testdatensatz für ihr Projekt selbst herstellen und statisch im Programmcode verwenden
- praktisch per JavaScript eine _Public API_ des Backends aufrufen und die Rückantwort auf der Entwicklerkonsole ausgeben

?- Demo: Vertiefung Strapi und REST-Client

- die Funktionsweise von JSON-Web-Token (JWT) erläutern
- praktisch private REST APIs durch Verwendung eines JWT in eigenständigem API-Client konsumieren
- praktisch mit Strapi-Relationen experimentieren und Abfragen durch Parameter wie `populate` erweitern
- praktisch Datenmodell im Frontend an das Datenmodell der Strapi-Antwort anpassen

## Termin 7 [(Lokale) LLMs & Agentic AI 🤖](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/07-llm-agents/01.md) (JB)

### Lernziele

- nutzen zur Problemlösung verschiedene Inferenz-Dienste
- verstehen aus Anwendersicht die Softwarearchitektur rund um "generative KI"-Services
- richten praktisch einen Coding Agenten ein
- können erläutern wozu RAG und MCP dienen
- setzen sich mit ethischen Fragestellungen auseinander

## Termin 8 [Software Testing ✅](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/08-testing/) (MT)

- Software Validierung & Verifikation inkl. Fragen
- Demo: Cypress, Vitest, Bruno

### Lernziele

- die Unterschiede zwischen Typen der Software-Verifikation/-Validierung (Unit-, Feature-, System-, Release-Tests) benennen
- ( verstehen weshalb fortgeschrittene Entwickler\*innen _Test-driven Development_ (TDD) als Methodologie einsetzen )
- praktisch eigenständig Code Reviews durchführen
- praktisch eine Test-Automation einrichten

## Termin 9 [DevOps kennenlernen](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/09-devops-ci/01.md) ♾️ (JB)

- DevOps organisatorisch und technisch
- Hands-on: Persönlicher Fork und Gitlab-Pipeline

### Lernziele

- den Begriff CI/CD (Continous Integration/Deployment) und die Funktion eines Integrationservers erklären
- praktisch einen Fork eines bestehenden Git-Repositories machen und die Unterschiede zwischen _downstream_ und _upstream_ erklären
- praktisch eine automatisierte Gitlab Pipeline anhand einer vorgegebenen Datei .gitlab-ci.yml einrichten und die Dokumentation für Anpassungen konsultieren

## Termin 10 [Cloudbasierte Software ☁ / DevOps Abschluss ⚙️🔍](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/10-cloud-devops-cd/) (MT)

- DevOps: Operation & Monitoring

### Lernziele

- den Einsatz der verschiedenen as-a-Service Angebote bezogen auf ein (Software)Produkt beurteilen können und die Vor- und Nachteile beschreiben
- Probleme und Gefahren beim Einsatz von as-a-Service Angeboten erläutern und für das eigene Praxisprojekt abschätzen
- die Begriffe Virtualisierung und Containerisierung, sowie die Eigenschaften von Cloudsoftware erklären

## Termin 11 [Accessibility 🦾🧏‍🦯 / Software Evaluation 📝](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/11-a11y-evaluation/01.md)

### Lernziele

- die Bedeutung von Zugänglichkeit/Accessibility für Webtechnologien erläutern und deren Herausforderungen bei der Implementierung diskutieren
- Vorteile des _Universal Design_ für heterogene Benutzergruppen nennen
- praktisch eine Website auf die Einhaltung der _Web Content Accessibility Guidelines_ (WCAG) überprüfen

## Termin 12 [Projektabschluss 🏁 / Gastbeitrag aus Praxis oder Forschung 🧑🏼‍🏭🧑🏼‍🔬](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/12-finishing/00.md) (JB)

- technischer Probelauf Prüfungsumgebung mit CAMPLA
- Reihenfolge Präsentationen festlegen

### Lernziele

- unterschiedliche Arten und Qualitäten eines Projektabschlusses in Bezug auf die Stakeholder benennen und erläutern
- Unterschiede zwischen den Prinzipien _Definition of Done_ und _Definition of Ready_ erläutern
- praktisch die erlaubten Software-Hilfsmittel der Theorieprüfung in einem Probelauf ausprobieren und eigene Materialien im PDF-Format für das Open-Book-Szenario vorbereiten
- praktisch eine gute Live-Demonstration des Teamprojekts vorbereiten und die bestehende Dokumentation anpassen, damit diese aussagekräftig für interessierte Dritte ist
- praktisch auf Gitlab-Pages die Frontend-Applikation publizieren (ohne Backend!)

## Termin 13 [Projektpräsentationen 👨🏼‍🏫👩🏼‍🏫 / Fragen zur Prüfung❓](https://github.com/digital-sustainability/module-wseg/blob/26/hs/docs/slides/content/13-final/) (MT/JB)

- Ort: Aula oder Greenfield ⛳
- Agile Aktivität
- Nachbesprechung Evaluationsergebnisse, Retrospektive
- Fragen zur Prüfung
- festgelegte Gruppenreihenfolge
