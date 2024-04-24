# Software Engineering

## #08 DevOps ♾️ + Cloud

WSEG / FS24<br />

[Source](https://github.com/digital-sustainability/module-wseg/tree/24/fs/docs/slides/content/08) licensed under [CC-BY-4.0](https://github.com/digital-sustainability/module-wseg/blob/main/LICENSE)

--

1. Rückblick
2. Demo: Angular + Strapi
3. Verständnis "DevOps" 📚
   - organisatorisch
   - technisch
4. Hands-on "Persönliches" git 🛠️
5. "Operations und Cloudbasierte (open source) Software"

--

### Rückblick

- Merge-Requests
  - kann MR nachträglich [geöffnet werden?](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/8352)
- Reminder MentorBot (Ioana hat "[contributet](https://github.com/digital-sustainability/module-wseg/commit/ae553c577b554b57340c74d68de878313099edbb)")
  - reflektierte Fragen ins Forum oder persönlich an Dozierende
- Fragen euerseits?

---

### Demo: Angular-HTTP -> Strapi-Restaurant

siehe Repository als Vorlage

---

### Begriff "DevOps"

- bezeichnet eine IT-Kulturtechnik
- Kofferwort aus "Development" und "IT Operations"
- 2009 von Patrick Debois geprägt
- [Anekdote](https://boingboing.net/2016/06/08/coder-fired-after-6-years-for.html) aus gleicher Zeit

--

### Ausgestaltungen

<img src="https://web.devopstopologies.com/images/2019-07-30--DOTs-types-thumb.png" height="400px" />

[Gelebte Team-Topologien](https://web.devopstopologies.com/#team-topologies)

--

### Werte dahinter: CA(L)MS

- Culture
- Automation
- (Lean)
- Measurement
- Sharing

[erläuterte Details](https://www.atlassian.com/de/devops/frameworks/calms-framework), [Incident Metriken](https://www.atlassian.com/de/incident-management/kpis/common-metrics)

--

#### Andere Kombinationen

- [DevSecOps](https://about.gitlab.com/topics/devops/)
- [GitOps](https://about.gitlab.com/topics/gitops/)
- BizDev(Ops)
  - [Paper 2017](https://www.sciencedirect.com/science/article/abs/pii/S0164121215001430?via%3Dihub)

---

### Stages / Continous Workflow ♾️

<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Devops-toolchain.svg" height="400px" />

oder PLAN, CODE, BUILD, TEST, RELEASE, DEPLOY, OPERATE, MONITOR

--

### lokale Entwicklungsumgebung vs. automatisierter Integrationsserver

--

### CI / CD

<img src="https://miro.medium.com/v2/resize:fit:2000/format:webp/1*57INuyf56018l0Y_Pel0ig.png" height="600px" />

---

<!-- .slide: data-background="#fff5c1" -->

### Hands-on: Gitlab Page mit Pipeline

#### im persönlichen Namespace erzeugen

- Unterschied **forken** 🍴 zu clonen

  - "Personal Project" unter https://gitlab.ti.bfh.ch/abcd1/
  - Original ist _upstream_, der Fork **downstream**

- "Pull-Request":
  - Anfrage an upstream..
  - ..Änderungen von downstream zu integrieren

--

<!-- .slide: data-background="#fff5c1" -->

### .. Basis für 4. Deliverable

```
 * "Page" veröffentlichen auf Gitlab
   * CI-Pipeline kennenlernen
   * Konvertierung Markdown -> HTML
```

- Bitte [ci-demo](https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-24-fs/ci-demo/) nach abcd1 forken

[Gitlab: CI Quickstart](https://docs.gitlab.com/ee/ci/quick_start/)

---

### Demo: Das Frontend bauen

- Was macht "npm build"?

--

### SPA-Frontend auf Gitlab Pages deployen

```yml
# ...Vorbereitungsteil wird auch benötigt!
pages:
 script:
- cd frontend
- npm run build
 artifacts:
 paths:
 - frontend/dist
 publish: frontend/dist
```

(Github nennt das [Actions](https://github.com/actions/) )

---

### Fragen?

> Wie interagieren automatisierte Problemverfolgungssysteme mit anderen Aspekten der DevOps-Automatisierung im Hinblick auf die Verbesserung der Effizienz und Zuverlässigkeit des gesamten SE-Prozesses?

- [Issue-Ablauf](https://youtu.be/kTNfi5z6Uvk?feature=shared&t=1530)
- [Beispiel zum Nachspielen](https://gitlab.com/missionimpossiblecode/what-and-why-of-devops/what-and-why-devops-instructions-and-exercises/-/blob/main/.gitlab/issue_templates/Lab%202%20See%20CI%20In%20Action.md?ref_type=heads)
- [Git-Commit schliesst Issue](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)

---

### Passwörter im Quellcode ⚠️

[Gitlab: Secret Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/)

#### Lösung: Secrets in CI-Variablen

z.B. für Deployment-Tokens, ...<br />
[Gitlab: CI Variables](https://docs.gitlab.com/ee/ci/variables/)

### Incident? Git-history verändern

[Github: Removing Sensitive Data](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

---

### Sicherheitslücken, Compliance Lizenzmodelle

- [internes Beispiel: Vulnerability Report](https://gitlab.ti.bfh.ch/digital-sustainability-lab/edp/-/security/vulnerability_report)
- [internes Beispiel: Verwendete Lizenzen](https://gitlab.ti.bfh.ch/digital-sustainability-lab/edp/-/licenses)

---

### Ausblick

- #9 Software Validierung (MT)
  - Zwischenpräsentation 2./3. Mai 👩🏼‍‍🏫
  - ggf. Coaching 2
- #10 📺 (Auffahrt)
- #11 Accessibility & UX Design (Tommi 🇫🇮)
  - ggf. Coaching 3

--

#### Zwischenpräsentation

- Rückblick und Ausblick

  - Welche Ziele haben wir uns für das Produkt gesetzt?
  - Bisher erreicht / Anpassungen der Ziele?
  - Grössten Schwierigkeiten?

- Live Demonstration

- Fragen
  - mindestens zwei vorbereitete Fragen um Feedback einzuholen.
    (dazu sind auch Onlinetools einsetzbar)
