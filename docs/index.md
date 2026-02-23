# Software-Engineering

[zum Quell-Repository](https://github.com/digital-sustainability/module-wseg)
![GitHub](https://img.shields.io/github/license/digital-sustainability/module-wseg)

## Wichtige Links

- Moodle Kurs: https://moodle.bfh.ch/course/view.php?id=42191
- BigBlueButton: https://bbb.ch-open.ch/rooms/bpp-2fr-o9h-eiw/join
- BFH-GitLab: https://gitlab.ti.bfh.ch/w-wseg/26-fs
- Wiki Page: [in gemeinsamer GitLab-Gruppe für Iterations Wrap-Ups](https://gitlab.ti.bfh.ch/groups/w-wseg/26-fs/-/wikis/home)

# Inhalte

🏗️ Hinweis: Kursinhalte in Veränderung, Inhalte des letzten Semesters sind teilweise noch verlinkt.

## #1 [Einführung und Überblick 🚀](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/01/01.md) (JB/MT remote)

- Überblick Modul
- Vorstellung & Kennenlernen
- Administratives: Praxisprojekt und Prüfung
- (Einführung Software Engineering)
- Werkzeuge und Accounts, Terminalbasics
- Gruppenbildung und erste Projektidee

### Lernziele

- praktisch auf ihrem Arbeitsgerät Software aus unterschiedlichen Quellen via Paketmanager installieren und nach Anleitung einrichten
- praktisch im Terminal bzw. ihrer jeweiligen Shell zwischen Ordnern wechseln und Befehle mit Parametern ausführen

## #2 [Codemanagement 🗃️](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/02/) (MT)

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

## #3 [Frontend: Webtechnologien 🌐](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/03/01.md) (JB)

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

## #4 [Backend: Softwarearchitektur / Einführung Strapi ✈️ 📦](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/04/) (JB)

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

## #5 [Agiles Arbeiten 🎯 / API Client verwenden](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/05/) (MT)

### Iteration 1: Wrap-up

- Infos zu Markdown und Merge-Requests (für 2. Deliverable)

### Lernziele

- die Prinzipien agiler Vorgehensweisen diskutieren und dafür Anwendungsmöglichkeiten im eigenen Berufsfeld erkennen (Überprüfbarkeit ? Weiter präzisieren)
- praktisch REST APIs durch einen eigenständigen API-Client testen bzw. verwenden
- praktisch das Format Markdown als Auszeichnungssprache für Dokumentationen in Gitlab verwenden
- praktisch in Git einen Branch für einen Merge-Request eröffnen und diesen nach dem _Code Review_ durch die Dozierenden selbständig zusammenführen

## #6 [Vue State Management, Axios JWT 🛠️ / TypeScript, OOP ⌨](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/06/) (JB)

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

## #7 [Vue State Management / Axios JWT 🛠️](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/07/) (JB)

- Demo: Vertiefung Strapi und REST-Client

### Lernziele

- die Funktionsweise von JSON-Web-Token (JWT) erläutern
- praktisch private REST APIs durch Verwendung eines JWT in eigenständigem API-Client konsumieren
- praktisch mit Strapi-Relationen experimentieren und Abfragen durch Parameter wie `populate` erweitern
- praktisch Datenmodell im Frontend an das Datenmodell der Strapi-Antwort anpassen

## [#8 Software Testing ✅](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/08/) (MT)

### Iteration 2: Wrap-up

- Software Validierung & Verifikation inkl. Fragen
- Demo: Cypress, Vitest, Bruno

### Lernziele

- die Unterschiede zwischen Typen der Software-Verifikation/-Validierung (Unit-, Feature-, System-, Release-Tests) benennen
- ( verstehen weshalb fortgeschrittene Entwickler\*innen _Test-driven Development_ (TDD) als Methodologie einsetzen )
- praktisch eigenständig Code Reviews durchführen
- praktisch eine Test-Automation einrichten

## [#9 DevOps kennenlernen](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/09/) ♾️🛠️ ☁ (JB)

- DevOps organisatorisch und technisch
- Hands-on: Persönlicher Fork und Gitlab-Pipeline

### Lernziele

- den Begriff CI/CD (Continous Integration/Deployment) und die Funktion eines Integrationservers erklären
- praktisch einen Fork eines bestehenden Git-Repositories machen und die Unterschiede zwischen _downstream_ und _upstream_ erklären
- praktisch eine automatisierte Gitlab Pipeline anhand einer vorgegebenen Datei .gitlab-ci.yml einrichten und die Dokumentation für Anpassungen konsultieren

## [#10 Accessibility and UX Design](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/08/) (Tommi Saksa)

### Lernziele

- die Bedeutung von Zugänglichkeit/Accessibility für Webtechnologien erläutern und deren Herausforderungen bei der Implementierung diskutieren
- Vorteile des _Universal Design_ für heterogene Benutzergruppen nennen
- praktisch eine Website auf die Einhaltung der _Web Content Accessibility Guidelines_ (WCAG) überprüfen

## [#11 Cloudbasierte Software ☁ / DevOps Abschluss ⚙️🔍](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/11/) (MT)

### Iteration 3: Wrap-up

- DevOps: Operation & Monitoring

### Lernziele

- den Einsatz der verschiedenen as-a-Service Angebote bezogen auf ein (Software)Produkt beurteilen können und die Vor- und Nachteile beschreiben
- Probleme und Gefahren beim Einsatz von as-a-Service Angeboten erläutern und für das eigene Praxisprojekt abschätzen
- die Begriffe Virtualisierung und Containerisierung, sowie die Eigenschaften von Cloudsoftware erklären

## [#12 Projektabschluss 🏁 / Prüfungsumgebung](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/12/) (JB)

- technischer Probelauf Prüfungsumgebung mit CAMPLA
- Reihenfolge Präsentationen festlegen

### Lernziele

- unterschiedliche Arten und Qualitäten eines Projektabschlusses in Bezug auf die Stakeholder benennen und erläutern
- Unterschiede zwischen den Prinzipien _Definition of Done_ und _Definition of Ready_ erläutern
- praktisch die erlaubten Software-Hilfsmittel der Theorieprüfung in einem Probelauf ausprobieren und eigene Materialien im PDF-Format für das Open-Book-Szenario vorbereiten
- praktisch eine gute Live-Demonstration des Teamprojekts vorbereiten und die bestehende Dokumentation anpassen, damit diese aussagekräftig für interessierte Dritte ist
- praktisch auf Gitlab-Pages die Frontend-Applikation publizieren (ohne Backend!)

## #13 Puffer je nach Bedarf

## [#14 Projektpräsentationen 👨🏼‍🏫👩🏼‍🏫 / Fragen zur Prüfung❓](https://github.com/digital-sustainability/module-wseg/blob/25/hs/docs/slides/content/14/) (MT/JB)

### Iteration 4: Abschlusspräsentation mit Live-Demo

- Ort: Greenfield ⛳
- Agile Aktivität
- Nachbesprechung Evaluationsergebnisse, Retrospektive
- Fragen zur Prüfung
- ab x.xx Uhr, festgelegte Gruppenreihenfolge
