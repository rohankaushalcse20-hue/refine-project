---
title: Introduction
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Ce tutoriel vous accompagne des bases de Refine jusqu'aux sujets plus avancés. Vous apprendrez à construire une application CRUD complète avec Refine.

Refine est agnostique au router : choisissez la bibliothèque que vous connaissez le mieux. Refine prend officiellement en charge [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) et [Remix](/core/docs/routing/integrations/remix). Les étapes suivantes afficheront le contenu correspondant à votre choix, que vous pouvez modifier à tout moment.

Choisissez la bibliothèque de routing à utiliser :

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

Dans les unités suivantes, vous sélectionnerez aussi une intégration UI de Refine. Même si Refine prend en charge Ant Design, Material UI, Mantine et Chakra UI, ce tutoriel se concentre sur les deux bibliothèques les plus utilisées : [Ant Design](/core/docs/ui-integrations/ant-design/introduction) et [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Choisissez le framework UI à utiliser :

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Vous trouverez le contenu équivalent pour les autres bibliothèques UI dans la [documentation](/core/docs/guides-concepts/ui-libraries).

## Contenu du tutoriel

### Fondamentaux

- [Votre première application Refine](/core/tutorial/essentials/setup/)
- [Récupérer un enregistrement](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Mettre à jour un enregistrement](/core/tutorial/essentials/data-fetching/updating-data/)
- [Lister des enregistrements](/core/tutorial/essentials/data-fetching/listing-data/)
- [Formulaires](/core/tutorial/essentials/forms/)
- [Tables](/core/tutorial/essentials/tables/)

### Authentification

- [Introduction](/core/tutorial/authentication/intro/)
- [Protéger le contenu](/core/tutorial/authentication/protecting-content/)
- [Connexion et déconnexion](/core/tutorial/authentication/logging-in-out/)
- [Utiliser l'identité utilisateur](/core/tutorial/authentication/user-identity/)
- [Intégration avec le data provider](/core/tutorial/authentication/data-provider-integration/)

### Routing avec React Router

- [Introduction](/core/tutorial/routing/intro/react-router/)
- [Authentification](/core/tutorial/routing/authentication/react-router/)
- [Définir les resources](/core/tutorial/routing/resource-definition/react-router/)
- [Navigation](/core/tutorial/routing/navigation/react-router/)
- [Inférer les paramètres](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirections](/core/tutorial/routing/redirects/react-router/)
- [Synchroniser l'état avec l'URL](/core/tutorial/routing/syncing-state/react-router/)

### UI avec Ant Design

- [Introduction](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Utiliser les layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [Composants CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentification](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### UI avec Material UI

- [Introduction](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Utiliser les layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [Composants CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentification](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

</Sandpack>
