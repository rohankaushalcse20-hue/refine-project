---
title: "Overview | Refine v5"
display_title: "Overzicht"
sidebar_label: "Overzicht"
description: "Leer het idee achter Refine kennen voordat je React-applicaties bouwt die sterk op CRUD zijn gericht."
displayed_sidebar: mainSidebar
slug: /getting-started/overview
---

**Refine** is een headless framework om snel datarijke React-applicaties te bouwen. Het brengt de terugkerende behoeften van admin panels, interne tools, dashboards, B2B-portalen en CRUD-workflows samen in een consistente architectuur: data ophalen, formulieren, tabellen, routing, authentication en authorization.

Refine laat de UI-laag onder jouw controle. Je kunt Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS of je eigen design system gebruiken, of volledig headless blijven met `@refinedev/core`.

## Waarom Refine?

- **Headless core:** gedrag voor data, state en navigation staat los van het UI-framework.
- **Provider-architectuur:** `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` en router provider maken integraties vervangbaar.
- **CRUD-productiviteit:** gedeelde patronen voor bewerkingen zoals `list`, `show`, `create`, `edit` en `clone`.
- **Praktijkscenario's:** ondersteuning voor filtering, pagination, optimistic updates, realtime, audit logs en multi-tenancy.

## Basisstructuur

Refine-applicaties worden meestal gemodelleerd rond `resources` en `providers`. `resources` beschrijven de domeinentiteiten; `providers` verbinden de applicatie met data, authenticatie, notificaties en routing.

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

## Volgende stappen

Maak een nieuw project via [Quickstart](/core/docs/getting-started/quickstart/). Begin daarna met [General Concepts](/core/docs/guides-concepts/general-concepts/) en [Data Fetching](/core/docs/guides-concepts/data-fetching/) om de architectuur beter te begrijpen.
