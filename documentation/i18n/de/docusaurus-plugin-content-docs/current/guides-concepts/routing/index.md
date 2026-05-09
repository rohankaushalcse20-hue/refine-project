---
title: "Routing | Refine v5"
display_title: "Routing"
sidebar_label: "Routing"
description: "Richte Routing in Refine mit React Router, Next.js, Remix oder einem kompatiblen System ein."
---

Routing ist fuer jede CRUD-Anwendung zentral. Die Headless-Architektur von Refine laesst dir die Wahl beim Router und bindet dich nicht an ein einzelnes Framework.

Refine bietet eingebaute Integrationen fuer **React Router**, **Next.js** und **Remix**. Diese Integrationen helfen dabei, Parameter automatisch zu erkennen, Redirects nach Mutationen oder Login-Status zu verarbeiten und Navigations-Utilities einheitlich zu verwenden.

Refine bleibt dennoch router-agnostisch. Du definierst deine Routen selbst: in React Router ueber `Routes`, in Next.js ueber `pages` oder `app` und in Remix ueber `app/routes`.

## Router Provider einbinden

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import routerProvider from "@refinedev/react-router";
import { BrowserRouter, Routes } from "react-router";

export const App = () => (
  <BrowserRouter>
    <Refine routerProvider={routerProvider}>
      <Routes>{/* deine Routen */}</Routes>
    </Refine>
  </BrowserRouter>
);
```

Halte Routen und Resources konsistent, damit Refine `resource`, `id` und weitere Parameter direkt aus der URL ableiten kann.
