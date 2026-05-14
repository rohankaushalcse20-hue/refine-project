---
title: "Démarrage rapide | Premiers pas avec Refine v5"
display_title: "Guide de démarrage rapide"
sidebar_label: "Démarrage rapide"
description: "Créez un projet Refine v5 avec le scaffolder navigateur ou la CLI, puis poursuivez vers les tutoriels."
displayed_sidebar: mainSidebar
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import { Playground } from "@site/src/components/playground";

**Refine** fonctionne dans tout environnement capable d'exécuter **React**, notamment Vite, Next.js, Remix et CRA.

Vous pouvez installer les packages manuellement, mais la façon recommandée de commencer consiste à utiliser le scaffolder navigateur ou la CLI. Les deux permettent de choisir le framework, l'UI, le data provider, l'authentification et l'i18n avant la génération du projet.

## Utiliser la CLI

Exécutez `create-refine-app` pour générer un projet avec des options guidées :

```sh
npm create refine-app@latest
```

Après avoir répondu aux questions, entrez dans le dossier généré, installez les dépendances si nécessaire et lancez le serveur de développement avec la commande indiquée par la CLI.

## Utiliser le navigateur

Le scaffolder navigateur propose les mêmes décisions principales que la CLI et permet de prévisualiser le résultat avant de le télécharger.

<Playground />

## Étapes suivantes

Continuez avec les [tutoriels](/core/tutorial) pour transformer le projet initial en application CRUD complète, consultez les [exemples réels](/core/templates) ou lisez les guides [concepts généraux](/core/docs/guides-concepts/general-concepts/) et [data fetching](/core/docs/guides-concepts/data-fetching/).
