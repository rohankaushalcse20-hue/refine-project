---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Scopri route definitions, resource navigation e integrazioni router provider nelle applicazioni Refine."
---

Refine non blocca il routing su un solo router. Può funzionare con React Router, Next.js, Remix o un router personalizzato, mantenendo i comportamenti di navigation basati su resource in un modello comune.

## Router provider

Il router provider permette a Refine di comunicare con il sistema di route dell'applicazione. Comportamenti come `go`, `back`, `parse`, `Link` e simili sono astratti attraverso questo provider.

## Resources e route

I campi `list`, `show`, `edit` e `create` nelle definizioni di resource descrivono le route CRUD dell'applicazione. Refine usa queste informazioni per navigation helpers, breadcrumb, menu e redirect.

```tsx title=App.tsx
import { Refine } from "@refinedev/core";

export const App = () => (
  <Refine
    resources={[
      {
        name: "posts",
        list: "/posts",
        show: "/posts/:id",
        edit: "/posts/:id/edit",
        create: "/posts/create",
      },
    ]}
  />
);
```

## Navigation helpers

`useGo`, `useBack`, `useNavigation` e i componenti button delle integrazioni UI usano le definizioni di resource per indirizzare l'utente alla route corretta. Questo riduce la dispersione di stringhe di route nel codice.

## Parametri

I segmenti dinamici si definiscono con parametri come `:id`. Refine può leggere dalla route attiva le informazioni su resource e action, così le pagine `show`, `edit` o `list` sanno con quale record lavorare.

## State sincronizzato

Filtri, sort e pagination delle liste possono essere sincronizzati con l'URL. Questo rende le viste condivisibili e mantiene coerente il comportamento della browser history.
