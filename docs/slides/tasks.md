# Deliverables

## 2 - [glab](https://docs.gitlab.com/ee/editor_extensions/gitlab_cli/) commandline

```bash

glab issue create \
 --title "Deliverable 2: Blogbeitrag mit Merge-Request" \
 --description " \
 `echo " \
Zum 'Due date' wird ein **Blogbeitrag mit 'Merge Request' als Deliverable** verlangt. Dieser sollte einen Rückblick über den aktuellen Stand und die Herausforderungen geben. Zeigt ggf. ein paar Screenshots eurer aktuellen Applikation und diskutiert die von euch gesetzten Datenmodelle und deren Anpassungen. (Auch geeignete Materialien aus der Präsentation könnt ihr wiederverwenden).\n \
\n \
Inhalt: Folgende Fragen sollte der Blogbeitrag beantworten:\n \
1. Welche **Ziele für die Applikation** haben wir uns als Gruppe gesetzt?\n \
    - Kurze **Beschreibung der Produktidee** mit den wichtigsten Features\n \
2. Auf welche **Hindernisse / Schwierigkeiten** sind wir bereits gestossen?\n \
    - Ist die **Erreichung des Ziels gefährdet**?\n \
    - Welche **Massnahmen** haben wir getroffen oder geplant **um diese Hindernisse zu beseitigen**?\n \
3. Wie ist der **Entwicklungsstand der Applikation**?\n \
    - **Datenmodelle und ggf. Testdaten** beschreiben.\n \
    - Ggf. **Screenshots** zeigen und beschreiben\n \
    - Ggf. **umgesetzte/geplante Features zeigen** und beschreiben\n \
    - Ebenfalls könnt ihr den **Techstack (Frontend, Backend, ggf. Dritt-CSS-Frameworks, ..)** thematisieren, welchen ihr bereits verwendet oder verwenden wollt.\n \
4. **Aufgabenverteilung im Team** beschreiben\n \
\n \
**Umfang**: min. 750 - 1250 Worte (Masstab: 250 Worte pro Teammitglied)\n \
\n \
**Format: Markdown** (Name z.B. Deliverable2-Blog.md) welches direkt in Gitlab verwendet werden kann. Dies ermöglicht eingebettete Bilder (z.B. im Unterorder "assets"), sowie Hyperlinks zu externen Ressourcen bzw. auch gitlab-intern. Als Referenz und Beispiel dient: https://gitlab.com/gitlab-org/gitlab/-/blob/master/doc/user/markdown.md \n \
\n \
**Git-Aufgabe Merge-Request**: Aus diesem vorbereiteten Issue "Deliverable 2" eröffnet ihr einen **Merge-Request**. Dieser erstellt in Git den **Branch "deliverable-2"** eures Repositories für die Markdown-Datei mitsamt verknüpften Inhalten (im Dokumentationsordner), so dass ihr wenn alles **commited (bzw. auch per CLI gepusht)** wurde, schliesslich **@tem1 und @bkj1 als Reviewer** für den MR hinzufügt. (… Nach Ablauf der Frist werden die Reviewer den MR mit "main" zusammenführen.)\n \
\n \
Als Referenz dient: https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html?tab=Merge+request+and+branch#from-an-issue \n \
\n \
Der Blog-Beitrag mitsamt Merge-Request muss spätestens zum oben angegebenen Datum bis 23:59 Uhr im Repository ersichtlich sein.
"`"  --label important --no-editor -R dsl-student-projects/agiles-arbeiten

```

## 3 - [glab](https://docs.gitlab.com/ee/editor_extensions/gitlab_cli/) commandline

```bash

for group in {4p-llcc,glink,4p-lesfribourgeois,4p-tillwedie,4o-Passionsfrucht,4o-gruppenname,4p-8,4p-http418,4p-http429,4p-paj,praxisprojekt-setup,4o-lar,4o-thoerims_goerkemousse}; do glab issue create \
 --title "Deliverable 3: Zwischenpräsentation mit Feedback" \
 --description " \
 `echo " \
Das dritte Deliverable ist eine **Präsentation** zum 'Due date': Sie sollte einen kurzen Rückblick über die bisherige Entwicklung und eine Live-Demo beinhalten und mit einigen Fragen ans Publikum enden. Bereitet die Fragen vor der Präsentation vor, damit ihr die Chance für Feedback optimal nutzen könnt.\n \
\n \
Eure Präsentation sollte **maximal 7 min** dauern. Die kurze Fragerunde findet nach der Präsentation statt.\n \
\n \
Inhalt:\n \
1. Rückblick und Ausblick\n \
    - Welche Ziele haben wir uns für das Produkt gesetzt?\n \
    - Welche Ziele haben wir bis jetzt erreicht?\n \
    - Welche Anpassungen an den Zielen mussten wir machen?\n \
    - Wo hatten wir bis jetzt die grössten Schwierigkeiten?\n \
2. ggf. Live Demonstration z.B. bereits erreichte Ziele anhand der User Stories demonstrieren.\n \
3. Fragen: Mindestens zwei vorbereitete Fragen um Feedback einzuholen - dazu können auch Onlinetools eingesetzt werden! \n \
\n \
Ladet die **Folien als PDF (ggf. auch Quellformat)** ins Git Repository bis spätestens 23:59 Uhr am Präsentationstag auf den Main Branch.
"`"  --label important --no-editor -R dsl-student-projects/wseg-24-fs/$group; done

```