# Ably-Integration fuer refine

`@refinedev/ably` stellt einen Ably-basierten `liveProvider` fuer Refine-Anwendungen bereit. Damit kannst du Echtzeit-Aktualisierungen, gemeinsame Arbeitsoberflaechen und Live-Dashboards an Refines Provider-Schnittstelle anbinden.

## Installation

```sh
npm install @refinedev/ably
```

## Grundlegende Verwendung

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

Nutze dieses Paket, wenn Datensaetze, Benachrichtigungen oder kollaborative Ansichten in deiner Refine-App live aktualisiert werden sollen.

Weitere Informationen findest du in der [Live-Provider-Dokumentation](https://refine.dev/docs/api-references/providers/live-provider/) und im [Ably-Tutorial](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine).
