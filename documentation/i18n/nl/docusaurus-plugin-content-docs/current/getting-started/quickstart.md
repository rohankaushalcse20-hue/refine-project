---
title: "Quickstart | Refine v5"
display_title: "Quickstart"
sidebar_label: "Quickstart"
description: "Maak en start je eerste Refine-applicatie met de officiële projectgenerator."
displayed_sidebar: mainSidebar
slug: /getting-started/quickstart
---

Deze quickstart laat zien hoe je een nieuwe Refine-app maakt, de ontwikkelserver start en de eerste resource verkent. De snelste route is de officiële generator, omdat die routing, data provider en UI-integratie alvast correct configureert.

## Nieuw project maken

Gebruik `npm create refine-app@latest` en volg de vragen in de terminal. De generator kan een headless app maken of direct een UI-framework zoals Ant Design, Material UI, Mantine of Chakra UI toevoegen.

```bash
npm create refine-app@latest my-refine-app
```

Ga daarna naar de projectmap en start de ontwikkelserver:

```bash
cd my-refine-app
npm run dev
```

## Wat wordt aangemaakt?

Een standaard Refine-project bevat een `Refine` root component, een router provider, een data provider en een eerste resourceconfiguratie. Die onderdelen vormen samen de basis voor CRUD-schermen.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
    resources={[
      {
        name: "products",
        list: "/products",
      },
    ]}
  />
);
```

## Volgende stappen

- Voeg resources toe voor de entiteiten in je eigen domein.
- Kies of vervang de UI-integratie die bij je project past.
- Configureer `authProvider`, `accessControlProvider` en `notificationProvider` wanneer je app login, rechten of gebruikersfeedback nodig heeft.

Lees daarna [General Concepts](/core/docs/guides-concepts/general-concepts/) voor de bouwstenen en [Routing](/core/docs/guides-concepts/routing/) voor route-integratie.
