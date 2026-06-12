# Iterations

## using [glab](https://docs.gitlab.com/ee/editor_extensions/gitlab_cli/) commandline in [zsh](https://www.zsh.org/)

```bash
for i in $(seq -w 01 14); do \
glab issue create \
 --title "Gruppe bilden und Gitlab Projekt anlegen - Gruppe $i" \
 --description " \
 `echo " \
Als Dozenten (@bkj1, @tem1) des Kurses WSEG im FS26 möchten wir im Gitlab pro Gruppe ein einzelnes Projekt und eine Wiki-Projektseite vorfinden, um die Personen und ihren individuellen Gruppenfortschritt über das Semester transparent begleiten zu können:\n \
- [ ] Alle Mitglieder auf diese Issue **assignen**\n \
- [ ] Projekt- bzw. Gruppennamen festlegen (enthält nicht &quot;WSEG&quot; oder &quot;Gruppe&quot;) und diese Issue umbenennen\n \
\n \
Spätestens an Termin 2 bitte:\n \
- [ ] [neues, leeres Gitlab Projekt](https://docs.gitlab.com/ee/user/project/#create-a-blank-project) als Kind der Gruppe [W-WSEG FS26](https://gitlab.ti.bfh.ch/w-wseg/26-fs/) anlegen\n \
  - [ ] [Projekttitel und -slug](https://docs.gitlab.com/ee/user/reserved_names.html#limitations-on-usernames-project-and-group-names-and-slugs) identisch wählen, dabei bitte **kein WSEG** im Namen verwenden\n \
- [ ] Neue Wiki-Seite mit Gruppenname anlegen unter https://gitlab.ti.bfh.ch/groups/w-wseg/26-fs/-/wikis/home , verwendet dazu das Template &apos;Gruppen Vorlage&apos; und listet bereits alle Teammitglieder auf. \n \
- [ ] [Alle Teammitglieder aktivieren Projekt-Benachrichtigung 🔔](https://docs.gitlab.com/user/profile/notifications/#change-level-of-project-notifications) \n \
  - [ ] Mitglied 1 beobachtet\n \
  - [ ] Mitglied 2 beobachtet\n \
  - [ ] Mitglied 3 beobachtet\n \
  - [ ] Mitglied 4 beobachtet\n \
  - [ ] Mitglied 5 beobachtet\n \
- [ ] [Avatarbilder aller Teammitglieder setzen](https://docs.gitlab.com/ee/user/profile/#access-your-user-profile) \n \
  - [ ] Avatar 1 gesetzt\n \
  - [ ] Avatar 2 gesetzt\n \
  - [ ] Avatar 3 gesetzt\n \
  - [ ] Avatar 4 gesetzt\n \
  - [ ] Avatar 5 gesetzt\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/sandbox \
; done
```

```bash
for i in $(seq -w 01 10); do \
glab issue create \
 --title "Gitlab Projekt: SSH Zugriff einrichten - Gruppe $i" \
 --description " \
 `echo " \
Richtet bitte bei jedem Teammitglied, für einen reibungslosen Zugriff auf alle Quellcode-Inhalte, des Kurses WSEG im FS26 einen, falls noch nicht vorhanden, entsprechenden SSH-Schlüssel ein und hinterlegt ihn in eurem jeweiligen Gitlab-Profil:\n \
- [ ] [lokale SSH-Keys generieren](https://git-scm.com/book/de/v2/Git-auf-dem-Server-Erstellung-eines-SSH-Public-Keys)\n \
  - [ ] Teammitglied 1 SSH-Key generiert\n \
  - [ ] Teammitglied 2 SSH-Key generiert\n \
  - [ ] Teammitglied 3 SSH-Key generiert\n \
  - [ ] Teammitglied 4 SSH-Key generiert\n \
  - [ ] Teammitglied 5 SSH-Key generiert\n \
- [ ] [SSH-Keys im Gitlab Profil hinterlegen](https://docs.gitlab.com/ee/user/ssh.html#add-an-ssh-key-to-your-gitlab-account)\n \
  - [ ] Teammitglied 1 SSH-Key hinterlegt\n \
  - [ ] Teammitglied 2 SSH-Key hinterlegt\n \
  - [ ] Teammitglied 3 SSH-Key hinterlegt\n \
  - [ ] Teammitglied 4 SSH-Key hinterlegt\n \
  - [ ] Teammitglied 5 SSH-Key hinterlegt\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/sandbox \
; done
```

## Layout

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
  for i in {0..4}; do \
    glab issue create \
      --title "Iteration $i - Rituale und Vorbereitung des Wrap-Ups" \
      --description " \
`echo " \
 - Führt bitte ein [Iteration Review](https://scaledagileframework.com/iteration-review/) durch.\n \
 - Plant bitte eure kommende Iteration im Rahmen eines [Iteration Plannings](https://scaledagileframework.com/iteration-planning/) in Form eines vorbereiteten Iterations [Team Backlogs](https://scaledagileframework.com/team-backlog/).\n \
 - Reflektiert bitte die aktuelle Iteration im Rahmen einer [Iteration Retrospective](https://scaledagileframework.com/iteration-retrospective/) und haltet eure Learnings und Anpassungen fest.\n \
 - [ ] Bitte hinterlegt alle notwendigen Informationen (Texte, Links, Screenshots, etc.) schlagwortartig im [gemeinsamen Wiki](https://gitlab.ti.bfh.ch/groups/w-wseg/26-fs/-/wikis/home): dieses nutzt ihr im Rahmen des Plenums als Vorstellungs- bzw. Präsentationsmedium. Erweitert dazu am besten jeweils einfach eure Wiki-Seite pro &quot;Iteration Wrap-Up&quot;. \n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group && \
    glab issue create \
      --title "Iteration $i - Wrap-Up: Review + Planung + Retrospektive" \
      --description " \
`echo " \
Bitte präsentiert euer Team &quot;Iteration Wrap-Up&quot; im Plenum anhand [Wiki](https://gitlab.ti.bfh.ch/groups/w-wseg/26-fs/-/wikis/home) und dem aktuellen Stand eures MVP (max. 15'):\n \
 - [ ] Iteration Review: bitte stellt die fachlichen Ergebnisse eurer aktuellen Iteration vor.\n \
 - [ ] Iteration Planning: bitte stellt die Planung eurer kommenden Iteration vor.\n \
 - [ ] Iteration Retrospective: bitte stellt eure Learnings und Anpassungen aus der aktuellen Iteration vor.\n \
\n \
Feedback (0-6 Punkte) zum Wrap-Up (auszufüllen von den Dozierenden: @bkj1, @tem1)\n \
- [ ] Review (1 P)\n \
  - [ ] technischer & fachlicher Fortschritt (1 P)\n \
- [ ] Planning (1 P)\n \
  - [ ] realistische Ziele (1 P)\n \
- [ ] Retrospektive (1 P)\n \
  - [ ] gelebter KVP (1 P)\n \
- [ ] Fragen / Feedback\n \
  - Fragestellung\n \
  - Feedback\n \
\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group
   ; done \
; done
```

# Deliverables

## ♻️ Iteration 0

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 0: Pitch der Projektidee" \
 --description " \
 `echo " \
Als Dozierende (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des ersten 'Iteration Wrap-Ups' einen gemeinsamen, ersten Einblick eurer Projektidee bekommen. (Hinweis: Beim ersten Mal werden **keine Punkte** vergeben!)\n \
\n \
Im Rahmen des Iterations-Reviews präsentiert ihr eure Produktidee in maximal 5min. Stellt euch vor ihr seid auf der Suche nach Finanzierung und euer Publikum besteht aus Investoren oder Mitgliedern eines Förderfonds.\n \
\n \
Wenn eure Präsentation und die Produktidee folgende Fragen beantwortet seid ihr gut unterwegs:\n \
 - Welches Problem/Bedürfnis haben eure Nutzer&midast;innen?\n \
 - Wie versucht euer Produkt dieses Problem zu lösen?\n \
 - Welches sind eure Nutzergruppen? Erstellt doch zwei Personas dazu. \n \
 - Was sollen Nutzer&midast;innen in eurer Applikation machen können? (Hier könnt ihr ggf. erste Wireframes, Mock-ups oder Prototypen zeigen)\n \
\n \
Ihr habt freie Wahl der Präsentationsmittel (Wiki-Seite, Powerpoint, Figma, Canva, Slides.com ...).\n \
 - [ ] Bei Verwendung externer Werkzeuge, ladet bitte die Folien als PDF (ggf. zusätzlich auch im Quellformat) in einen neuen Unterordner **docs** eures Git-Repository bis spätestens 23:59 Uhr des Präsentationstags. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group
; done
```

## ♻️ Iteration 1

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
lab issue create \
 --title "Deliverable 1: Erstes MVP und User Feedback einholen" \
 --description " \
 `echo " \
Als Dozierende (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-up 1** ein erstes Minimal-Viable-Product bestehend aus zwei Seiten bzw. Ansichten sehen, welches idealerweise bereits in einem JavaScript-Framework wie z.B. Vue.js erstellt wurde. Bitte verzichtet für dieses Deliverable auf Fertiglösungen, welche durch KI-Prompts generiert wurden!\n \
- [ ] Startseite euer Plattform mit Link oder Aktion innerhalb eines Webbrowsers \n \
- [ ] Eine zweite Seite bzw. Ansicht eines Formulars, welches später zum Einloggen oder zur Nutzerregistrierung weiterentwickelt werden kann. (Für das Wechseln zwischen Ansichten/Funktionen innerhalb einer Single-Page-Application wird die Verwendung eines Routers, wie z.B. [router.vuejs.org](https://router.vuejs.org/) empfohlen) \n \
\n \
Neben dem praktischen Einstieg des Teams ins Projekt soll diese Vorstellung die Gelegenheit geben, um Rückmeldungen des Publikums einzuholen:\n \
- [ ] Auswahl an passenden Farben/Farbvarianten/Bildelementen/Logos treffen und Feedback dazu einholen\n \
- [ ] Falls der Name eures Produkts noch nicht entschieden ist, könntet ihr ebenfalls Varianten vorstellen und dafür ein Stimmungsbild erhalten\n  \
\n \
Individuelle Aufgabe:\n \
- [ ] Jedes Teammitglied hat auf dem main-Branch mindestens **einen Commit** gepusht. Es genügt wenn dieser bspw. nur aus einer Änderung der Datei README.md besteht. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group
; done
```

## ♻️ Iteration 2

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 2: Blogbeitrag und Datenmodell mit Merge-Request" \
 --description " \
 `echo "\
Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-Up 2** einen kurzen Blogbeitrag im Repository vorfinden. Dieser sollte einen Rückblick über den aktuellen Stand und die Herausforderungen geben. (_Stand MVP_: Wahrscheinlich habt ihr zu diesem Zeitpunkt eine erste Anbindung des Frontends ans Backend durch Nutzerregistrierung und/oder Loginfunktionalität geschafft) \n \
- [ ] Blogbeitrag im Markdown-Format, idealerweise im docs-Ordner, \n \
  - [ ] mindestens eine Bilddatei (z.B. Logo, Screenshot o.ä.) aus Repository eingebettet \n \
  - [ ] Link zu einer [Bruno-Collection](https://gitlab.ti.bfh.ch/w-wseg/26-fs/sandbox/-/tree/main/backend/bruno?ref_type=heads), die aufzeigt wie euer erstes, grundlegendes Datenmodell über die API abgefragt werden kann und wie Einträge per POST erstellt werden können
- [ ] unter Verwendung des GitLab-Features Merge-Request \n \
\n \
Inhalt: Folgende Fragen sollte der Blogbeitrag beantworten:\n \
1. Welche **Hauptziele für die Applikation** habt ihr euch als Gruppe gesetzt?\n \
    - Kurze Beschreibung der Produktidee mit den wichtigsten User Stories\n \
2. Aktueller **Entwicklungsstand der Applikation**?\n \
    - Verwendet ihr Testdaten (Mockdata), die im Code integriert sind?\n \
    - Zeigt ggf. auch **Screenshots** des aktuellen Stands\n \
3. Beschreibt eure Organisation und die **Aufgabenverteilung im Team**:\n \
    - z.B. wie gestaltet ihr euren Wissenstransfer?\n \
    - ... was sind eure aktuellen Herausforderungen?\n \
\n \
**Format: Markdown** (Name z.B. Deliverable2-Blog.md), kann direkt im Gitlab-Frontend zur Textformatierung verwendet werden. Es ermöglicht das Einfügen von Bildern (z.B. im Unterorder &quot;assets&quot;) und die Verwendung von Hyperlinks (externe Ressourcen oder auch Gitlab-intern). Als Referenz und Beispiel dient: https://gitlab.com/gitlab-org/gitlab/-/blob/master/doc/user/markdown.md \n \
\n \
**Due date:** Der Blog-Beitrag und die Bruno-Collection sollen im Merge-Request bis spätestens zum oben angegebenen Wrap-Up bis 23:59 Uhr im Repository ersichtlich sein.\n \
\n \
**Git-Aufgabe Merge-Request**: Aus dieser vorbereiteten Issue &quot;Deliverable 2&quot; eröffnet ihr einen **Merge-Request**. Dieser erstellt in Git einen **Branch &quot;123-deliverable-2...&quot;** eures Repositories, welcher zum Hinzufügen aller benötigten Dateien verwendet werden soll. Sobald vollständig gebt ihr **@tem1 und @bkj1 als Reviewer** für den MR an. (… Nach Ablauf der Frist geben die Reviewer ihr &quot;Approval&quot; und danach führt ihr selbständig den MR mit dem Branch &quot;main&quot; zusammen.\n \
Als Referenz dient: https://docs.gitlab.com/user/project/merge_requests/creating_merge_requests/?tab=Merge+request+and+branch#from-an-issue )\
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group \
; done
```

## ♻️ Iteration 3

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 3: Gitlab Page per CI Pipeline" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-up 3** euren vorherigen Blogbeitrag als Gitlab-Page vorfinden. Dazu verwendet ihr das CI-Beispiel aus der [Sandbox](https://gitlab.ti.bfh.ch/w-wseg/26-fs/sandbox/) für euer Gruppenrepository. \n \
- [ ] Deaktiviert die Funktion &apos;Use unique domain&apos;, damit das Ergebnis unter https://w-wseg.pages.ti.bfh.ch/26-fs/repository-name/ (für authentifizierte User) sichtbar ist und platziert die URL für das Wrap-up auf euer Wikiseite \n \
  - [ ] Eure README.md sollte wie im Beispiel selbst als _index.html_ fungieren und ebenfalls einen funktionierenden, relativen Link zum Blogpost enthalten \n \
  - [ ] Bilder, welche im Markdown-Blogbeitrag verlinkt wurden, müssen im Build-Job z.B. nach public/docs kopiert werden \n \
- [ ] Richtet in der Pipeline eine weitere Stage vor der Textkonvertierung ein, in der zuerst eure [Markdown-Dateien gelintet](https://gitlab.ti.bfh.ch/w-wseg/module/-/blob/26/fs/docs/slides/content/09-devops-ci/01.md?ref_type=heads&plain=1#L317) werden. Dieser Job darf fehlschlagen und dient nur zur Information.
- [ ] Verwendet im _.gitlab-ci.yml_ die Regel, dass die Pipeline nur ausgeführt wird, wenn die Commit-message die Worte  &rdquo;Blog&rdquo; oder  &rdquo;Readme&rdquo; (Gross-/Kleinschreibung ignorieren) enthält, um unnötigen Ressourcenverbrauch zu vermeiden. (_&dollar;CI_COMMIT_MESSAGE =~ /blog/i || &dollar;CI_COMMIT_MESSAGE =~ /readme/i_ &ndash; Als Referenz dient: https://docs.gitlab.com/ee/ci/jobs/job_rules.html)\n \
\n \
Überlegt bitte welche Arc42-[Qualitätskriterien](https://gitlab.ti.bfh.ch/w-wseg/module/-/blob/5101b9cd48b737f09e50ab09e2fd6f87a350d5d3/docs/slides/content/11/criteria.md) inkl. Schwerpunkt und welche Features ihr für euer Praxisprojekt aussuchen werdet, um diese im Wrap-up benennen zu können. \n \
- [ ] Haltet diese voraussichtliche Auswahl auf euer Wikiseite fest: **Tabellarische Vorlage in Markdown** \n \
~~~ \n \
|  self-chosen | link or description  | \n \
|---|---| \n \
|  Quality Property 1 |   | \n \
|  Quality Property 2 |   | \n \
|  Quality Property 3 |   | \n \
|  Schwerpunkt |   | \n \
|  Feature 1 |   | \n \
|  Feature 2 |   | \n \
~~~ \n \
 \n \
**Due date:** Eure konvertierten Dokumente müssen spätestens zum oben angegebenen Wrap-up bis 23:59 Uhr per Gitlab Pages ersichtlich sein. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group \
; done
```

## ♻️ Iteration 4

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "WICHTIG: individuelle WSEG-Modulevaluation ausfüllen bis ... ‼️" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir und unser Institutsleiter (@smm15) anonyme und ehrliche **quantitative Ergebnisse** zu unseren Kursdurchführungen erhalten, um zukünftig Verbesserungen vornehmen zu können. Wir erinnern hiermit **alle Teammitglieder**, sofern noch nicht bereits erledigt: \n \
 1. Bitte die **E-Mail** von _EVASYS_ zum Modul WSEG **suchen**,
 1. auf den Umfragelink **klicken** und
 1. _mindestens den quantitativen_ Teil zu Unterricht und Dozierenden **ausfüllen**.
 1. **Vielen, herzlichen Dank** 🙏🏼 (_qualitative Freitextantworten sind optional und fliessen in die gemeinsame Retrospektive mit ein_) \n \
\n \
**Due date:** Der Befragungszeitraum ist bis Montag, 1. Juni 23:59 Uhr geöffnet. \n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group \
; done
```

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Abschlusspräsentation: Live-Demo und Retrospektive" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir in der letzten Veranstaltung eine **maximal 15-minütige Abschlusspräsentation** erleben. Bei der Wahl der Präsentationsmittel seid ihr frei, ebenso welche Teammitglieder vortragen. Darin sollte eine gut vorbereitete Demonstration enthalten sein, welche den wichtigsten Funktionsumfang anhand einer oder mehrerer User-Journeys aufzeigt (ggf. Registrieren oder Einloggen / Inserieren / zweiten User in anderem Browser einloggen / Kontakt aufnehmen o.ä.). Eine Vorstellung der Ergebnisse euer Rituale _Review_ und _Planning_ ist nicht mehr notwendig. \n \
- vorgeschlagene Inhalte: \n \
  - [ ] Ursprüngliche Businessidee, Organisation Team, ... \n \
  - [ ] Live-Demo (+ ggf. Erläuterung externer APIs/Frameworks) \n \
  - [ ] Reflexion eures Arbeitsprozesses, Learnings für zukünftige Projekte \n \
  - [ ] optional: Aufhänger als Einstieg / Interaktion / ... \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group \
; done
```

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
--title "Deliverable 4: aktualisierte README und SPA-Deployment auf Gitlab Pages" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir spätestens eine Woche nach Modulabschluss eine **aktualisierte README** und eure **Single-Page-Application** (nur das Frontend!) **auf Gitlab-Pages** vorfinden. \n \
 \n \
 Hinweis: Es ist dabei unerheblich, wenn Inhalte aus dem Backend fehlen werden. Weiterhin brauchen auch keine [CORS](https://de.wikipedia.org/wiki/Cross-Origin_Resource_Sharing)-Regeln definiert werden, welche ggf. Zugriff auf eine lokal gestartete API-Instanz zulassen. \n \
- W-Fragen in README.md klären: \n \
  - [ ] Wozu kann eure App verwendet werden? \n \
  - [ ] Welchen Techstack für Frontend und Backend habt ihr verwendet? \n \
  - [ ] Welche 3rd-Party Libraries (z.B. _Axios_) habt ihr für das Projekt nachträglich installiert? \n \
  - [ ] Wie kann das Projekt von neuen Entwickler\*innen aufgesetzt werden? (Beschreibt die Schritte von &apos;git clone&apos; bis zu &apos;npm run dev(elop)&apos;). Dieser Artikel gibt gute Anhaltspunkte: https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/ \n \
 \n \
- Ergänzt eure README durch die [Arc42-Vorlage aus der Sandbox](https://gitlab.ti.bfh.ch/w-wseg/26-fs/sandbox/-/blob/main/README.md#mvp): \n \
  - [ ] inkl. der selbstgewählten [Qualitätskriterien](https://gitlab.ti.bfh.ch/w-wseg/module/-/blob/26/fs/docs/slides/content/11/criteria.md) \n \
  - [ ] und belegt beispielhaft alle Kriterien durch Verlinkung des Codes mit Zeilennummern oder Screenshots \n \
- Stellt eure SPA über eine CI/CD Pipeline bereit: \n \
\n \
  - [ ] ... Hilfestellungen dazu sind in [den Folien von Termin 9](https://gitlab.ti.bfh.ch/w-wseg/module/-/blob/26/fs/docs/slides/content/09-devops-ci/01.md?ref_type=heads&plain=1#L189-L196)\n \
    - [ ] Falls benötigt: Instead of altering &apos;vite.config.js&apos;, it is possible to pass &apos;--base&apos; to &apos;vite build&apos;: or concerning &apos;npm run build -- --base=&dollar;CI_PAGES_URL&apos; [Quelle Stackoverflow](https://stackoverflow.com/questions/75837088/set-vite-base-via-gitlab-ci-pages-url-variable) \n \
  - [ ] Im &apos;.gitlab-ci.yml&apos; sollt ihr eine Regel erstellen, dass die neue(n) Stage(s) nur ausgeführt werden, wenn über das Gitlab-UI der Run-Button gestartet wird (&apos;when: manuals&apos;) oder eine entsprechende Commit-message eintrifft \n \
  - [ ] Verlinkt eure Demosite (z.B. Artefakte im Pages-Pfad &apos;/demo/&apos;) ebenfalls in der README \n \
\n \
**Due date:** Die erwähnten Gitlab-Pages sind spätestens 7 Tage nach dem Modulabschluss (letzte Semesterwoche) verfügbar. Dies ist ebenso der Zeitpunkt des spätesten Commits, welcher für die Beurteilung des Praxisprojekts gilt. \n \
\n \
**Projektabschluss 🏁:** Seid stolz auf eure gemeinsamen Leistungen dieses Semesters! Nach der schriftlichen Abschlussprüfung erhaltet ihr via IS-Academia auf offiziellem Wege eure individuelle Modulnote. Auf Anfrage wird die Bewertung des gemeinsamen Projekts mitgeteilt. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/w-wseg/26-fs/$group \
; done
```
