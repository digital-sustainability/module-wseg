# Software Engineering

## #08 DevOps ♾️ + Cloud

WSEG / FS24<br />

[Source](https://github.com/digital-sustainability/module-wseg/tree/24/fs/docs/slides/content/08) licensed under [CC-BY-4.0](https://github.com/digital-sustainability/module-wseg/blob/24/fs/LICENSE)

--

1. Rückblick
2. Demo: Angular + Strapi
3. Verständnis "DevOps" 📚
   - organisatorisch
   - technisch
4. Hands-on "Persönliches" git 🛠️
5. "Operations und Cloudbasierte Systeme"

--

### Rückblick

- Merge-Requests
  - kann MR nachträglich [geöffnet werden?](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/8352)
  - DIY: Ready to merge! -> Delete source branch & merge
- Reminder MentorBot + Checkliste
  - reflektierte Fragen ins Forum oder persönlich an Dozierende
- JWT Intro (siehe Aufzeichnung)
- Fragen euerseits?

---

### Demo 🛠️

#### Angular-HTTP -> Strapi-Restaurant

--

### Angular v17 mit Standalone [(Quelle)](https://dev.to/this-is-angular/how-to-fetch-data-using-the-providehttpclient-in-angular-5h47)

#### app.config.ts

- `provider:` um `, provideHttpClient()` erweitern

### Service erstellen

- `ng g service service/restaurant`
- -> wird RestaurantService heissen..

--

### restaurant.service.ts

- HttpClient importieren
- .. und im Konstruktor initialisieren
- Hol-Funktion mit GET-Request:
  <br/><br/>

```
  getAllRestaurants() {
   return this.http.get('http://localhost:1337/api/restaurants');
 }

```

--

### app.component.ts

- RestaurantService importieren
- Datenmodell anhand Strapi-Antwort definieren:

```
interface Restaurant {
  id: number;
  attributes: {
    name: string;
    description: string;
  }
}
```

- ... damit leeren Array initialisieren:
  `  restaurants: Restaurant[] = [];`

--

### app.component.ts

- `restaurantService: RestaurantService = inject(RestaurantService)`
- **http**-Rückgabe ist ein `Observable`
- Array `restaurants` befüllen ab Key "data"

```
constructor() {
    this.restaurantService.getAllRestaurants().subscribe({
      next: (results: any) => {
        this.restaurants = results.data;
      },
      error: (error) => {
        console.log(error);
      },
      complete: () => {
        console.log("finished");
      }
    });
  }
```

--

### app.component.html

```
{{ title }} Demo

<ul *ngFor="let restaurant of restaurants">
  <li>{{ restaurant.attributes.name }}</li>
  <li>{{ restaurant.attributes.description }}</li>
</ul>
```

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

- [DevSecOps](https://about.gitlab.com/blog/2021/06/01/gitlab-is-setting-standard-for-devsecops/)
- [GitOps](https://about.gitlab.com/topics/gitops/)
- BizDev(Ops)
  - [Paper 2017](https://www.sciencedirect.com/science/article/abs/pii/S0164121215001430?via%3Dihub)

> ❓ Gibt es andere Methoden / Frameworks, die ähnliche Ziele wie DevOps verfolgen? Falls ja, ...

---

### Stages / Continous Workflow ♾️

<img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Devops-toolchain.svg" height="400px" />

oder PLAN, CODE, BUILD, TEST, RELEASE, DEPLOY, OPERATE, MONITOR

--

### lokale Entwicklungsumgebung

#### vs.

### automatisierter Integrationsserver

--

### CI / CD

<img src="https://miro.medium.com/v2/resize:fit:2000/format:webp/1*57INuyf56018l0Y_Pel0ig.png" height="600px" />

--

### ❓

> Welche Strategien und Werkzeuge würdest du empfehlen, um die Kluft zwischen Entwicklung (Dev) und Betrieb (Ops) in einem Unternehmen zu überbrücken und eine effektive DevOps-Kultur zu fördern?

---

### Beispiel: Single-Page-Application "updaten"

![](https://suresoft.dev/assets/workshops/continuous-integration/img/ci-gitlab.JPG)

- [Gitlab CI Pipeline](https://docs.gitlab.com/ee/ci/quick_start/)
  (Github nennt das [Actions](https://github.com/actions/) )

--

### Demo: ... für Produktionsumgebung bauen

- Was machen `ng build` bzw. `npm build`?
- z.B. TypeScript ➡️ JavaScript
- 📁 dist/.../browser mit:
  - index.html
  - main.js
  - polyfills.js
  - styles.css

--

#### Example: https://osamaelhariri.gitlab.io/TechBlog/

### Ausschnitt .gitlab-ci.yml

```yml
...
pages:
 script:
- cd frontend
- npm run build
 artifacts:
 paths:
 - frontend/dist/demo-app/browser
 publish: frontend/dist/demo-app/browser
```

--

### ❓

> Welche Vorteile bietet die kontinuierliche Integration im Kontext der DevOps-Automatisierung?

---

<!-- .slide: data-background="#fff5c1" -->

### Hands-on: Gitlab Page mit Pipeline

```
 * HTML-"Page" veröffentlichen auf Gitlab
   * CI-Pipeline kennenlernen
   * Konvertierung Markdown -> HTML
```

--

<!-- .slide: data-background="#fff5c1" -->

#### Fork im persönlichen Namespace

- Unterschied **forken** 🍴 zu clonen

  - Original ist _upstream_, der Fork **downstream**

- **Pull-Request**:
  - Eine Anfrage an upstream..
  - ..bestimmte Änderungen von downstream zu integrieren

--

<!-- .slide: data-background="#fff5c1" -->

### Kurze Übung 🛠️

#### ..als Basis für 4. Deliverable

https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-24-fs/ci-demo/

- Bitte [ci-demo](https://gitlab.ti.bfh.ch/dsl-student-projects/wseg-24-fs/ci-demo/) nach abcd1 forken
- wird "Personal Project"<br/>
  https://gitlab.ti.bfh.ch/abcd1/ci-demo/

---

### Fragen?

--

> Wie könnte die Implementierung von GitLab CI/CD in einem Startup die Produktentwicklungszyklen beeinflussen und welche praktischen Vorteile könnte das Team erwarten?

--

> Nachfrage: Was sind die wichtigsten Herausforderungen, denen sich Unternehmen bei der Einführung von KI und maschinellem Lernen stellen müssen und wie können diese überwinden werden?

---

### Passwörter im Quellcode ⚠️

[Gitlab: Secret Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/)

#### Lösung: Secrets in CI-Variablen

z.B. für Deployment-Tokens, ...<br />
[Gitlab: CI Variables](https://docs.gitlab.com/ee/ci/variables/)

--

### Incident? Git-history verändern

[Github: Removing Sensitive Data](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

--

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
