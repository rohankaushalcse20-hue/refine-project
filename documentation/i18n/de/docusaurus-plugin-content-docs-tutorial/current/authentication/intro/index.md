---
title: Einfuehrung
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Jetzt kennst du die Grundlagen fuer Data Fetching und Datenmanipulation in Refine. In dieser Einheit lernst du, wie du Authentifizierung zu deiner Anwendung hinzufuegst und wie die wichtigsten Authentifizierungsbausteine in Refine funktionieren.

Refine stellt eine leicht zu verwaltende Authentifizierungsschnittstelle bereit, die sich mit wenig Aufwand mit jedem Authentication Provider verwenden laesst.

Diese Einheit behandelt die folgenden Themen:

- Die Schnittstelle [`AuthProvider`](/core/docs/authentication/auth-provider) kennenlernen, indem wir einen Authentication Provider erstellen.
- Auth-Hooks und -Komponenten verwenden, zum Beispiel die Hooks [`useLogin`](/core/docs/authentication/hooks/use-login) und [`useIsAuthenticated`](/core/docs/authentication/hooks/use-is-authenticated) sowie die Komponente [`<Authenticated />`](/core/docs/authentication/components/authenticated).
- Authentifizierung in Data Providern behandeln und Authentifizierungsfehler verwalten.

Diese Einheit ist unabhaengig von Router und UI-Framework. Die zugehoerigen Authentifizierungsteile fuer Router und UI-Frameworks werden in den naechsten Einheiten behandelt.

</Sandpack>
