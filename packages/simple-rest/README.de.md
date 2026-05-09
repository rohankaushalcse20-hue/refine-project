# Simple-REST-Data-Provider

`@refinedev/simple-rest` stellt einen Data Provider fuer REST-APIs mit einer standardisierten Struktur bereit. Er orientiert sich am Stil von `json-server` und verbindet Refine-Resources mit HTTP-Endpoints.

## Installation

```sh
npm install @refinedev/simple-rest
```

## Grundlegende Nutzung

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

## Wann du ihn einsetzt

Nutze diesen Provider, wenn dein Backend einfache REST-Endpoints fuer Listen, Erstellen, Aktualisieren und Loeschen bereitstellt. Falls deine API Authentifizierung, eigene Header oder spezielle Parameter benoetigt, kannst du den Provider erweitern oder umhuellen.

## Mehr Informationen

Die Refine-Dokumentation zu Data Providern zeigt, wie du die Integration an dein Backend anpasst.
