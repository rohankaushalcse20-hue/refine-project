---
title: Deine erste Refine-App
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Eine neue Refine-App zu erstellen ist sehr einfach und braucht nur wenige Schritte, um eine funktionsfaehige Anwendung zu generieren. Fuer dieses Tutorial nutzen wir `create-refine-app` nicht mit allen Optionen. Stattdessen erstellen wir eine leere App, installieren die benoetigten Abhaengigkeiten und konfigurieren die App manuell.

<Tabs wrapContent={false}>

<TabItem value="quick" label="Schnelles Setup">

Um diesem Tutorial zu folgen, kannst du die Starter-Templates von `create-refine-app` verwenden. Der folgende Befehl erstellt ein neues leeres Projekt mit den Paketen `@refinedev/core` und `@refinedev/cli`; damit ist alles vorhanden, was du fuer den Einstieg in das Tutorial brauchst.

```sh
npm create refine-app@latest -- --example starter-vite
```

</TabItem>

<TabItem value="manual" label="Manuelles Setup">

Wir erstellen unsere App mit dem passenden Template. Danach installieren wir die Refine-Abhaengigkeiten und konfigurieren die Anwendung.

```sh
npm create vite@latest my-refine-app -- --template react-ts
```

Mehr ueber Vite und das Erstellen von Projekten findest du in der [Vite-Dokumentation](https://vitejs.dev/guide/#scaffolding-your-first-vite-project).

Nachdem das Projekt erstellt wurde, muessen wir die Refine-Abhaengigkeiten installieren.

```sh
npm install @refinedev/core @refinedev/cli
```

Wir installieren `@refinedev/core`, das alle Kernfunktionen von Refine bereitstellt, und `@refinedev/cli`. Die CLI ist optional, bietet aber viele nuetzliche Funktionen fuer den Entwicklungsprozess. Mehr ueber `@refinedev/cli` findest du in [der Dokumentation](/core/docs/packages/cli).

### Scripts konfigurieren

Wir ersetzen unsere Scripts `dev`, `build` und `serve` durch die folgenden Eintraege:

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

Die Runner-Befehle von `refine` verwenden intern dieselben Befehle wie der Bundler, fuegen aber nuetzliche Funktionen hinzu, etwa Versionspruefungen fuer Abhaengigkeiten und Ankuendigungen des Refine-Teams.

### App konfigurieren

Wir muessen die Komponente `<Refine />` in unserer App mounten. Wir haengen sie am Root der Anwendung ein.

```tsx title="src/App.tsx"
import { Refine, WelcomePage } from "@refinedev/core";

function App() {
  return (
    <Refine>
      <WelcomePage />
    </Refine>
  );
}

export default App;
```

Hier passiert nichts Besonderes. Wir mounten nur die Komponente `<Refine />` in unserer Anwendung. `<Refine />` ist die Kernkomponente von Refine und stellt den benoetigten Context sowie die Logik bereit, damit die App funktioniert.

Die Komponente `<WelcomePage />` wird von `@refinedev/core` bereitgestellt und zeigt eine einfache Willkommensseite fuer Refine an. Du kannst sie entfernen, wenn du moechtest.

Das reicht aus, um die App zu starten. Mit dem folgenden Befehl koennen wir die Anwendung ausfuehren:

```sh
npm run dev
```

Wenn du deinen Browser oeffnest und zu localhost navigierst, solltest du die Seite rechts sehen. Wenn alles wie erwartet funktioniert, fahre mit dem naechsten Abschnitt fort.

</TabItem>

</Tabs>

:::tip Massgeschneiderte App-Generierung

`create-refine-app` fuehrt dich standardmaessig durch einige Schritte, um eine neue App passend zu deinen Anforderungen zu erstellen: von Data Providern ueber Authentifizierung bis zu UI-Bibliotheken und mehr. Mehr dazu findest du im Abschnitt [Schnellstart](/core/docs/getting-started/quickstart).

:::

</Sandpack>
