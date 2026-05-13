---
title: "General Concepts | Refine v5"
display_title: "Concetti generali"
sidebar_label: "Concetti generali"
description: "Comprendi l'architettura headless di Refine e i concetti di resources, providers, hooks e meta."
---

Refine è un framework estendibile per creare rapidamente applicazioni web. La sua base è composta da **hooks** e **providers** componibili, con pattern chiari per gestire dati e state.

## Approccio headless

Refine non impone un set di componenti visivi. Fornisce `hooks`, `components`, `providers` e helper, mentre il livello UI resta sotto il tuo controllo.

Per questo puoi usare Tailwind CSS, Ant Design, Material UI, Mantine, Chakra UI o il tuo design system insieme a `@refinedev/core`.

## Concetto di resource

Un **Resource** rappresenta un'entità dell'applicazione, come `products`, `orders` o `blogPosts`. La definizione di resource collega route, operazioni CRUD, liste e providers in una struttura coerente.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "products",
        list: "/products",
        show: "/products/:id",
        edit: "/products/:id/edit",
        create: "/products/new",
      },
    ]}
  />
);
```

## Providers

I providers sono i principali punti di integrazione in Refine. Tramite providers, l'applicazione gestisce dati, authentication, authorization, notifications, i18n, routing, realtime e audit logs.

## Hooks

Gli hooks di Refine sono headless e non dipendono da una libreria UI specifica. Con `useGo`, `useCan`, `useTranslate` e altri hooks puoi gestire navigation, permessi e traduzioni tramite API uniformi.

## Meta

La proprietà `meta` viene usata per inviare informazioni aggiuntive a providers e hooks, ad esempio headers, parametri personalizzati, selezione dei campi o contesto multi-tenant.
