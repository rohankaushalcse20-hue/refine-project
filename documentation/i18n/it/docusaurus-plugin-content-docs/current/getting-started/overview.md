---
title: "Overview | Refine v5"
display_title: "Panoramica"
sidebar_label: "Panoramica"
description: "Scopri l'idea alla base di Refine prima di creare applicazioni React orientate al CRUD."
displayed_sidebar: mainSidebar
slug: /getting-started/overview
---

**Refine** è un framework headless per sviluppare rapidamente applicazioni React ricche di dati. Riunisce in un'unica architettura le esigenze comuni di pannelli admin, strumenti interni, dashboard, portali B2B e workflow CRUD: lettura dei dati, form, tabelle, routing, authentication e authorization.

Refine lascia a te il controllo del livello UI. Puoi usare Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS o il tuo design system, oppure restare completamente headless con `@refinedev/core`.

## Perché Refine?

- **Core headless:** i comportamenti di dati, state e navigation sono indipendenti dal framework UI.
- **Architettura a provider:** `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` e router provider rendono sostituibili le integrazioni dell'applicazione.
- **Produttività CRUD:** fornisce pattern condivisi per operazioni come `list`, `show`, `create`, `edit` e `clone`.
- **Scenari reali:** supporta filtering, pagination, optimistic updates, realtime, audit logs e multi-tenancy.

## Struttura di base

Le applicazioni Refine sono spesso modellate intorno a `resources` e `providers`. I `resources` descrivono le entità del dominio; i `providers` collegano l'applicazione a dati, autenticazione, notifiche e routing.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        create: "/products/new",
        edit: "/products/:id/edit",
        show: "/products/:id",
      },
    ]}
  />
);
```

## Prossimi passi

Per creare un nuovo progetto passa a [Quickstart](/core/docs/getting-started/quickstart/). Per comprendere meglio l'architettura, inizia da [General Concepts](/core/docs/guides-concepts/general-concepts/) e [Data Fetching](/core/docs/guides-concepts/data-fetching/).
