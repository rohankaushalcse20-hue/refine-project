---
title: Einfuehrung
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Dieses Tutorial fuehrt dich von den Grundlagen von Refine bis zu fortgeschrittenen Themen. Du lernst, wie du mit Refine eine vollstaendige CRUD-Anwendung aufbaust.

Refine ist routerunabhaengig; du kannst also die Routing-Bibliothek verwenden, mit der du am besten vertraut bist. Refine unterstuetzt offiziell [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) und [Remix](/core/docs/routing/integrations/remix). In den weiteren Schritten des Tutorials bekommst du Inhalte angezeigt, die zu deiner Routing-Auswahl passen. Du kannst deine Auswahl jederzeit aendern und dir waehrend des Tutorials die Inhalte fuer andere Bibliotheken ansehen.

Waehle die Routing-Bibliothek aus, mit der du fortfahren moechtest:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

In den weiteren Einheiten dieses Tutorials waehlst du eine UI-Framework-Integration von Refine aus und lernst, wie UI-Integrationen aufgebaut sind und wo sie nuetzlich sind. Refine unterstuetzt offiziell Ant Design, Material UI, Mantine und Chakra UI. Das Tutorial ist fuer die zwei am haeufigsten verwendeten UI-Frameworks vorbereitet: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) und [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Waehle das UI-Framework aus, mit dem du fortfahren moechtest:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Das entsprechende Material aus diesem Tutorial fuer andere UI-Frameworks findest du in der [Dokumentation](/core/docs/guides-concepts/ui-libraries).

## Tutorial-Inhalte

Unten findest du alle Tutorial-Abschnitte nach Themen geordnet:

### Grundlagen

- [Deine erste Refine-App](/core/tutorial/essentials/setup/)
- [Einen Datensatz abrufen](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Einen Datensatz aktualisieren](/core/tutorial/essentials/data-fetching/updating-data/)
- [Datensaetze auflisten](/core/tutorial/essentials/data-fetching/listing-data/)
- [Formulare](/core/tutorial/essentials/forms/)
- [Tabellen](/core/tutorial/essentials/tables/)

### Authentifizierung

- [Einfuehrung](/core/tutorial/authentication/intro/)
- [Inhalte schuetzen](/core/tutorial/authentication/protecting-content/)
- [An- und Abmelden](/core/tutorial/authentication/logging-in-out/)
- [Benutzeridentitaet verwenden](/core/tutorial/authentication/user-identity/)
- [Data-Provider-Integration](/core/tutorial/authentication/data-provider-integration/)

### Routing mit React Router

- [Einfuehrung](/core/tutorial/routing/intro/react-router/)
- [Authentifizierung](/core/tutorial/routing/authentication/react-router/)
- [Resources definieren](/core/tutorial/routing/resource-definition/react-router/)
- [Navigation](/core/tutorial/routing/navigation/react-router/)
- [Parameter ableiten](/core/tutorial/routing/inferring-parameters/react-router/)
- [Weiterleitungen](/core/tutorial/routing/redirects/react-router/)
- [State mit der Location synchronisieren](/core/tutorial/routing/syncing-state/react-router/)

### UI-Bibliotheken mit Ant Design

- [Einfuehrung](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Layouts verwenden](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [CRUD-Komponenten](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Benachrichtigungen](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentifizierung](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### UI-Bibliotheken mit Material UI

- [Einfuehrung](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Layouts verwenden](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [CRUD-Komponenten](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Benachrichtigungen](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentifizierung](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Naechste Schritte mit Ant Design

- [Einfuehrung](/core/tutorial/next-steps/intro/ant-design/)
- [Inferencer verwenden](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [CLI verwenden](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Devtools verwenden](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Zusammenfassung](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Naechste Schritte mit Material UI

- [Einfuehrung](/core/tutorial/next-steps/intro/material-ui/)
- [Inferencer verwenden](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [CLI verwenden](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Devtools verwenden](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Zusammenfassung](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
