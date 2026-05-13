---
title: Introduzione
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Questo tutorial ti porta gradualmente dalle basi di Refine a workflow più avanzati. Seguendo i passaggi, imparerai a costruire un'applicazione CRUD completa con Refine.

Refine non è legato a una sola libreria di routing, quindi puoi scegliere la soluzione più adatta al modo di lavorare del tuo team. Refine supporta ufficialmente [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) e [Remix](/core/docs/routing/integrations/remix). I contenuti successivi si adatteranno alla scelta di routing, che potrai comunque modificare più avanti.

Scegli la libreria di routing da seguire:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

Nel modulo successivo sceglierai anche l'integrazione UI e imparerai come è costruita e quando conviene usarla. Refine supporta ufficialmente Ant Design, Material UI, Mantine e Chakra UI, ma questo tutorial si concentra sui percorsi più comuni: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) e [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Scegli il framework UI da seguire:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

I contenuti per altre librerie UI sono disponibili nella [documentation](/core/docs/guides-concepts/ui-libraries).

## Contenuto del tutorial

Le sezioni seguenti sono raggruppate per argomento:

### Essentials

- [Prima applicazione Refine](/core/tutorial/essentials/setup/)
- [Recuperare un record](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Aggiornare un record](/core/tutorial/essentials/data-fetching/updating-data/)
- [Elencare record](/core/tutorial/essentials/data-fetching/listing-data/)
- [Forms](/core/tutorial/essentials/forms/)
- [Tables](/core/tutorial/essentials/tables/)

### Authentication

- [Introduzione](/core/tutorial/authentication/intro/)
- [Proteggere contenuti](/core/tutorial/authentication/protecting-content/)
- [Login e logout](/core/tutorial/authentication/logging-in-out/)
- [Usare l'identità utente](/core/tutorial/authentication/user-identity/)
- [Integrazione data provider](/core/tutorial/authentication/data-provider-integration/)

### Routing con React Router

- [Introduzione](/core/tutorial/routing/intro/react-router/)
- [Authentication](/core/tutorial/routing/authentication/react-router/)
- [Definizione resources](/core/tutorial/routing/resource-definition/react-router/)
- [Navigation](/core/tutorial/routing/navigation/react-router/)
- [Inferenza dei parametri](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirects](/core/tutorial/routing/redirects/react-router/)
- [Sincronizzare state con location](/core/tutorial/routing/syncing-state/react-router/)

### Librerie UI con Ant Design

- [Introduzione](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Usare layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [Componenti CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Librerie UI con Material UI

- [Introduzione](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Usare layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [Componenti CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Prossimi passi con Ant Design

- [Introduzione](/core/tutorial/next-steps/intro/ant-design/)
- [Usare Inferencer](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [Usare CLI](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Usare Devtools](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Riepilogo](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Prossimi passi con Material UI

- [Introduzione](/core/tutorial/next-steps/intro/material-ui/)
- [Usare Inferencer](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [Usare CLI](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Usare Devtools](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Riepilogo](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
