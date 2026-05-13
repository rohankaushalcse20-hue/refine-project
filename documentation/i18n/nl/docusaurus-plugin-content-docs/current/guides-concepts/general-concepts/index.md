---
title: "General Concepts | Refine v5"
display_title: "General Concepts"
sidebar_label: "General Concepts"
description: "Begrijp de kernconcepten achter Refine-applicaties: resources, providers, hooks en headless UI."
displayed_sidebar: mainSidebar
slug: /guides-concepts/general-concepts
---

Refine organiseert CRUD-applicaties rond een klein aantal herbruikbare concepten. Als je deze bouwstenen kent, kun je sneller bepalen waar data, routing, authenticatie en UI-gedrag thuishoren.

## Resources

Een `resource` beschrijft een domeinobject zoals `products`, `orders` of `users`. Je koppelt er routepaden en acties aan, bijvoorbeeld `list`, `create`, `edit` en `show`.

```tsx
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
```

## Providers

Providers verbinden Refine met de buitenwereld. Een `dataProvider` spreekt je API aan, een `routerProvider` synchroniseert routes, een `authProvider` beheert loginstatus en een `notificationProvider` toont feedback aan gebruikers.

Omdat providers gewone JavaScript-objecten zijn, kun je bestaande packages gebruiken of een eigen adapter schrijven voor je backend en ontwerpkeuzes.

## Hooks en componenten

Refine biedt hooks zoals `useList`, `useOne`, `useCreate`, `useUpdate` en `useDelete`. UI-packages bouwen daar componenten bovenop, maar de core blijft headless. Daardoor kun je dezelfde datalogica gebruiken met Material UI, Ant Design, Mantine, Chakra UI of je eigen componentbibliotheek.

## Aanbevolen leesroute

Begin met [Data Fetching](/core/docs/guides-concepts/data-fetching/) om de providercontracten te begrijpen. Lees daarna [Routing](/core/docs/guides-concepts/routing/), [Authentication](/core/docs/guides-concepts/authentication/) en [Authorization](/core/docs/guides-concepts/authorization/) voor applicatiebrede concerns.
