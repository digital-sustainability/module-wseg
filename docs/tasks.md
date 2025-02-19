# Iterations

## using [glab](https://docs.gitlab.com/ee/editor_extensions/gitlab_cli/) commandline in [zsh](https://www.zsh.org/)

```bash
for i in {1..5}; do \
glab issue create \
 --title "Gitlab Projekt anlegen - Gruppe 0$i" \
 --description " \
 `echo " \
Als Dozenten (@bkj1, @tem1) des Kurses WSEG im HS24 möchten wir im Gitlab pro Gruppe ein einzelnes Projekt vorfinden:\n \
- [ ] Projekt- bzw. Gruppennamen festlegen\n \
- [ ] [neues, leeres Gitlab Projekt](https://docs.gitlab.com/ee/user/project/#create-a-blank-project) als Kind der [dsl-student-projects/WSEG HS24](https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-24-hs) anlegen\n \
  - [ ] [Projekttitel und -slug](https://docs.gitlab.com/ee/user/reserved_names.html#limitations-on-usernames-project-and-group-names-and-slugs) identisch wählen\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/sandbox \
; done
```

## Layout

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
  for i in {0..4}; do \
    glab issue create \
      --title "Iteration $i - Review" \
      --description " \
`echo " \
Bitte bereitet ein kurzes, im Plenum stattfindendes, [Iteration Review](https://scaledagileframework.com/iteration-review/) vor.\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group && \
    glab issue create \
      --title "Iteration $i - Planung der nächsten Iteration" \
      --description " \
`echo " \
Bitte plant eure kommende Iteration im Rahmen eines [Iteration Plannings](https://scaledagileframework.com/iteration-planning/) in Form eines vorbereiteten Iterations [Team Backlogs](https://scaledagileframework.com/team-backlog/).\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group && \
    glab issue create \
      --title "Iteration $i - Retrospektive" \
      --description " \
`echo " \
Bitte reflektiert die aktuelle Iteration im Rahmen einer [Iteration Retrospective](https://scaledagileframework.com/iteration-retrospective/) und haltet eure Learnings und Anpassungen fest.\n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group && \
    glab issue create \
      --title "Iteration $i - Wrap-Up: Review, Planung, Retrospektive" \
      --description " \
`echo " \
Bitte bereitet euer Team "Iteration Wrap-Up" vor und präsentiert es im Plenum (max. 15'):\n \
 - [ ] Iteration Review: bitte stellt die fachlichen Ergebnisse eurer aktuellen Iteration vor.\n \
 - [ ] Iteration Planning: bitte stellt (kurz) die Planung eurer kommenden Iteration vor.\n \
 - [ ] Iteration Retrospektive: bitte stellt (kurz) eure Learnings und Anpassungen aus der aktuellen Iteration vor.\n \
\n \
Hinterlegt dazu bitte alle notwendigen Informationen (Texte, Links, Screenshots, etc.) schlagwortartig im gemeinsamen [Wiki](https://gitlab.ti.bfh.ch/groups/wseg-group-demo/-/wikis/home): dieses werdet ihr im Rahmen des Plenums als Vorstellungs- bzw. Präsentationsmedium nutzen. Legt dazu am besten jeweils einfach eine neue Wiki-Seite pro "Iteration Wrap-Up" an. \n \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group
   ; done \
; done
```

# Deliverables

## ♻️ Iteration 0

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Gitlab Projekt und Profil konfigurieren" \
 --description " \
 `echo " \
Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Gitlab ein Projekt vorfinden um die Personen und Ihren individuellen Gruppenfortschritt über das Semester transparent begleiten zu können:\n \
- [ ] [Teammitglieder hinzufügen](https://docs.gitlab.com/ee/user/project/members/#add-users-to-a-project) \n \
  - [ ] Teammitglied 1 hinzugefügt\n \
  - [ ] Teammitglied 2 hinzugefügt\n \
  - [ ] Teammitglied 3 hinzugefügt\n \
  - [ ] Teammitglied 4 hinzugefügt\n \
  - [ ] Teammitglied 5 hinzugefügt\n \
- [ ] [Avatare aller Teammitglieder setzen](https://docs.gitlab.com/ee/user/profile/#access-your-user-profile) \n \
  - [ ] Avatar 1 gesetzt\n \
  - [ ] Avatar 2 gesetzt\n \
  - [ ] Avatar 3 gesetzt\n \
  - [ ] Avatar 4 gesetzt\n \
  - [ ] Avatar 5 gesetzt\n \
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
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group && \
glab issue create \
 --title "Pitch der Projektidee" \
 --description " \
 `echo " \
Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des ersten 'Iteration Wrap-Ups' Review 0 einen gemeinsamen, ersten Einblick eurer Projektidee bekommen.\n \
\n \
Im Rahmen des Iterations-Reviews präsentiert ihr eure Produktidee in maximal 10min. Stellt euch vor ihr seid auf der Suche nach Finanzierung und euer Publikum besteht aus Investoren oder Mitgliedern eines Förderfonds.\n \
\n \
Zeigt dabei den aktuellen Stand der Entwicklungen durch Wireframes, Mock-ups oder sogar vielleicht durch einen ersten HTML/CSS-Prototyp. Ihr seid frei bei der Verwendung des Präsentationsmittels (Powerpoint, Canva, Figma, reveal.js ...).\n \
\n \
Wenn eure Präsentation und die Produktidee folgende Fragen beantwortet seid ihr gut unterwegs:\n \
 - Welches Problem haben meine Nutzer?\n \
 - Wie löst euer Produkt dieses Problem?\n \
 - Welches sind eure Nutzergruppen? Erstellt doch zwei Personas dazu. \n \
 - Was kann der Nutzer in eurer Applikation machen und wie kann er damit sein Problem lösen? (Hier könnt ihr eure Prototypen einsetzen)\n \
\n \
Ladet die Folien als PDF (ggf. zusätzlich auch das Quellformat) ins Git Repository bis am Präsentationstag 23:59 Uhr auf den Main Branch! \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group
; done
```

## ♻️ Iteration 1

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
lab issue create \
 --title "Deliverable 1: Erstes MVP und User Feedback einholen" \
 --description " \
 `echo " \
Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-up 1** ein erstes Minimal-Viable-Product bestehend aus zwei Seiten bzw. Ansichten sehen, welches idealerweise bereits in einem JavaScript-Framework wie z.B. Vue.js erstellt wurde. Neben dem praktischen Einstieg des Teams ins Projekt soll diese Vorstellung die Gelegenheit geben, um Rückmeldungen des Publikums einzuholen:\n \
- [ ] Startseite mit Link oder Aktion innerhalb eines Webbrowsers \n \
  - [ ] Eine zweite Seite bzw. Ansicht eines Formulars, welches später zum Einloggen oder zur Nutzerregistrierung weiterentwickelt werden kann \n \
  - [ ] (Für das Wechseln zwischen Ansichten/Funktionen innerhalb einer Single-Page-Application wird die Verwendung eines Routers, wie z.B. [router.vuejs.org](https://router.vuejs.org/) empfohlen \n \
- [ ] Auswahl an passenden Farben/Farbvarianten/Bildelementen/Logos treffen und Feedback dazu einholen\n \
- [ ] (Falls der Name eures Produkts noch nicht entschieden ist, könntet ihr ebenfalls Varianten vorstellen und dafür ein Stimmungsbild erhalten) \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group
; done
```

## ♻️ Iteration 2

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 2: Blogbeitrag mit Merge-Request" \
 --description " \
 `echo "\
Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-up 2** einen Blogbeitrag im Repository vorfinden. Dieser sollte einen Rückblick über den aktuellen Stand und die Herausforderungen geben. \n \
 - [ ] Blogbeitrag im Markdown-Format, Umfang ~1000 Worte, idealerweise im docs-Ordner \n \
  - [ ] enthält grundlegendes Datenmodell als Entity-Relationship Diagramm (nicht zu detailliert!) \n \
- [ ] Merge-Request dazu verwenden \n \
\n \
Inhalt: Folgende Fragen sollte der Blogbeitrag beantworten:\n \
1. Welche **Ziele für die Applikation** haben wir uns als Gruppe gesetzt?\n \
    - Kurze **Beschreibung der Produktidee** mit den wichtigsten Features\n \
2. Wie ist der **Entwicklungsstand der Applikation**?\n \
    - Beschreibt euer **Datenmodell** und ggf. Testdaten\n \
    - Ggf. aktuelle **Screenshots** zeigen (könnten auch Testdaten enthalten)\n \
    - Ggf. **umgesetzte/geplante Features zeigen** oder beschreiben\n \
    - Ebenfalls könnt ihr den **Techstack (Frontend, Backend, ggf. Dritt-CSS-Frameworks, ..)** thematisieren, welchen ihr bereits verwendet oder verwenden wollt.\n \
3. Auf welche **Hindernisse / Schwierigkeiten** sind wir bereits gestossen?\n \
    - Ist die **Erreichung des Ziels gefährdet**?\n \
    - Welche **Massnahmen** haben wir getroffen oder geplant **um diese Hindernisse zu beseitigen**?\n \
4. Die **Aufgabenverteilung im Team** und eure Organisation beschreiben z.B. wie gestaltet ihr euren Wissenstransfer?\n \
\n \
**Format: Markdown** (Name z.B. Deliverable2-Blog.md) welches direkt in Gitlab verwendet werden kann. Dies ermöglicht eingebettete Bilder (z.B. im Unterorder "assets"), sowie Hyperlinks zu externen Ressourcen bzw. auch gitlab-intern. Als Referenz und Beispiel dient: https://gitlab.com/gitlab-org/gitlab/-/blob/master/doc/user/markdown.md \n \
\n \
**Due date:** Der Blog-Beitrag (ohne Merge-Request) muss spätestens zum oben angegebenen Wrap-up bis 23:59 Uhr im Repository ersichtlich sein.\n \
\n \
**Git-Aufgabe Merge-Request**: Aus diesem vorbereiteten Issue "Deliverable 2" eröffnet ihr einen **Merge-Request**. Dieser erstellt in Git den **Branch "nummer-deliverable-2"** eures Repositories für die Markdown-Datei mitsamt verknüpften Inhalten (im Dokumentationsordner), so dass ihr wenn alles **committed (bzw. auch per CLI gepusht)** wurde, schliesslich **@tem1 und @bkj1 als Reviewer** für den MR hinzufügt. (… Nach Ablauf der Frist geben die Reviewer ihr "Approval" und ihr führt den MR mit "main" zusammen.\n \
Als Referenz dient: https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html?tab=Merge+request+and+branch#from-an-issue )\
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group \
; done
```

## ♻️ Iteration 3

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 3: Gitlab Page per CI Pipeline" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir im Rahmen des **Iteration Wrap-up 3** euren vorherigen Blogbeitrag als Gitlab-Page vorfinden. Dazu verwendet ihr das CI-Beispiel aus der [Sandbox](https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-24-hs/sandbox/) für euer Gruppenrepository. Die Funktionalitäten &apos;CI/CD&apos;, sowie &grave;Pages&grave; wurden für eure Repositories bereits aktiviert, der Gitlab-UI-Bug, welcher verhinderte dass ihr dies selbst tun konntet, wurde zwischenzeitlich sogar behoben. \n \
- [ ] Deaktiviert die Funktion Unique URL unter Deploy-Pages, damit das Ergebnis unter https://dsl-student-projects.pages.ti.bfh.ch/wseg-24-hs/repository-name/ für authentifizierte User sichtbar ist und platziert die URL für das Wrap-up auf euer Wikiseite) \n \
  - [ ] Eure README.md sollte wie im Beispiel selbst als index.html fungieren und ebenfalls einen funktionierenden Link zum Blogpost enthalten \n \
  - [ ] Bilder, welche im Markdown-Blogbeitrag verlinkt wurden, müssen in der Pipeline z.B. nach public/docs kopiert werden \n \
- [ ] Verwendet im .gitlab-ci.yml die Regel, dass die Pipeline nur ausgeführt wird, wenn die Commit-message die Worte Blog oder Readme (Gross-/Kleinschreibung ignorieren) enthält, um unnötigen Ressourcenverbrauch zu vermeiden. (&dollar;CI_COMMIT_MESSAGE =~ /blog/i || &dollar;CI_COMMIT_MESSAGE =~ /readme/i -- Als Referenz dient: https://docs.gitlab.com/ee/ci/jobs/job_rules.html)\n \
\n \
**Due date:** Der Blog-Beitrag muss spätestens zum oben angegebenen Wrap-up bis 23:59 Uhr auf Pages ersichtlich sein. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group \
; done
```

## ♻️ Iteration 4

```bash
for group in {praxisprojekt-01-demo,praxisprojekt-02-demo}; do \
glab issue create \
 --title "Deliverable 4: aktualisierte README und SPA-Deployment auf Gitlab Pages" \
 --description " \
 `echo "\
 Als Dozenten (@bkj1, @tem1) des Kurses WSEG möchten wir zur Abschlusspräsentation eine aktualisierte README und eure Single-Page-Application auf Gitlab-Pages vorfinden. \n \
- In README.md W-Fragen klären: \n \
  - [ ] Wozu kann eure App verwendet werden? \n \
  - [ ] Welchen Techstack für Frontend und Backend habt ihr verwendet? \n \
  - [ ] Welche 3rd-Party Libraries habt ihr eingesetzt? \n \
  - [ ] Wie kann das Projekt von neuen Entwickler*innen aufgesetzt werden? (Beschreibt die Schritte von &apos;git clone&apos; bis zu &apos;npm run dev(elop)&apos;). \n \
  - [ ] Wie lauten die Anmeldedaten für einen Strapi Admin-User? (Auch wenn dies ein Anti-Pattern darstellt, ist es sinnvoll diese für euch und die Dozierenden zu hinterlegen). \n \n \
Diese Anleitung gibt weitere gute Anhaltspunkte: https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/ \n \
 \n \
- Ergänzt eure README entsprechend der Vorlage (unter xyz): \n \
  - [ ]  betreffend der selbstgewählten [Qualitätskriterien](https://github.com/digital-sustainability/module-wseg/blob/24/hs/docs/slides/content/11/08.md) \n \
  - [ ] Belegt beispielhaft alle Kriterien durch Verlinkung des Codes mit Zeilennummern  \n \
- Stellt eure SPA über eine CI/CD Pipeline bereit: \n \
\n \
  - [ ] Hilfestellungen dazu im [Ausschnitt Folien #9](https://github.com/digital-sustainability/module-wseg/blob/a17343422f40552976d504ac297fb5b0aa2250d8/docs/slides/content/09/01.md?plain=1#L113-L143)\n \
  - [ ] Falls benötigt: Instead of altering &apos;vite.config.js&apos;, it is possible to pass &apos;--base&apos; to &apos;vite build&apos;: &apos;npm run build --base=&dollar;CI_PAGES_URL&apos;\n \
  - [ ] Im .gitlab-ci.yml könnt ihr eine Regel erstellen, dass die neue(n) Stage(s) nur ausgeführt werden, wenn über das Gitlab-UI der Run-Button gestartet wird (&apos;when: manuals&apos;) oder eine entsprechende Commit-message eintrifft \n \
  - [ ] Verlinkt eure Demosite ebenfalls in der README \n \
\n \
**Due date:** Die erwähnten Gitlab-Pages müssen spätestens zum oben angegebenen Präsentationtag bis 18.00 Uhr verfügbar sein. \
"`"  --label important --no-editor -R https://gitlab.ti.bfh.ch/wseg-group-demo/$group \
; done
```
