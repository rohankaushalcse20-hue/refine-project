---
title: Introduction
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Vous connaissez maintenant les bases du data fetching et des mutations dans Refine. Dans cette unité, vous apprendrez à ajouter l'authentification à l'application et à comprendre les fondamentaux de l'authentification dans Refine.

Refine fournit une interface d'authentification simple à maintenir, compatible avec presque tout provider d'authentification.

Cette unité couvre :

- L'interface [`AuthProvider`](/core/docs/authentication/auth-provider) en créant un provider d'authentification.
- L'utilisation de hooks et composants comme [`useLogin`](/core/docs/authentication/hooks/use-login), [`useIsAuthenticated`](/core/docs/authentication/hooks/use-is-authenticated) et [`<Authenticated />`](/core/docs/authentication/components/authenticated).
- La gestion de l'authentification dans les data providers et des erreurs liées à l'authentification.

Cette unité reste agnostique au router et à la bibliothèque UI. Les parties propres au router et à l'UI seront traitées dans les unités suivantes.

</Sandpack>
