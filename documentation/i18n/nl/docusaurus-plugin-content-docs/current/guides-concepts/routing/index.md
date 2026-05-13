---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Leer hoe Refine resources en acties koppelt aan routes zonder je routerkeuze te bepalen."
displayed_sidebar: mainSidebar
slug: /guides-concepts/routing
---

Routing in Refine verbindt resource-acties met echte URL's. Refine schrijft geen router voor; in plaats daarvan gebruik je een `routerProvider` voor React Router, Next.js, Remix of een eigen routerintegratie.

## Resources en routepaden

Elke resource kan paden definiëren voor `list`, `create`, `edit`, `show` en `clone`. Deze paden worden gebruikt door navigatiehelpers, breadcrumbs, redirect-logica en acties vanuit UI-componenten.

```tsx
<Refine
  resources={[
    {
      name: "posts",
      list: "/posts",
      create: "/posts/create",
      edit: "/posts/edit/:id",
      show: "/posts/show/:id",
    },
  ]}
/>
```

## Router provider

De `routerProvider` vertaalt Refine-acties naar de API van je router. Daardoor kunnen hooks zoals `useNavigation` en componenten zoals knoppen of menu-items hetzelfde blijven, ook als je routerstack verandert.

## Parameters en navigatie

Routes met dynamische segmenten, zoals `/posts/edit/:id`, ontvangen hun waarden via de router. Refine gebruikt deze informatie om de juiste resource, actie en record-id te bepalen.

## Praktische richtlijn

Houd resourcepaden dicht bij de `resources`-configuratie en laat pagina's vooral hun eigen UI en datalogica beheren. Dat maakt het eenvoudiger om routes te hernoemen zonder CRUD-gedrag door de hele app te verspreiden.
