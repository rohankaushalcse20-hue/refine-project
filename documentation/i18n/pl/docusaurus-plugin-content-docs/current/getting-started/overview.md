---
title: "Overview | Refine v5"
display_title: "Przegląd"
sidebar_label: "Przegląd"
description: "Poznaj ideę Refine, zanim zaczniesz budować aplikacje React nastawione na CRUD."
displayed_sidebar: mainSidebar
slug: /getting-started/overview
---

**Refine** to headless framework do szybkiego tworzenia bogatych w dane aplikacji React. Łączy w jednej architekturze typowe potrzeby paneli administracyjnych, narzędzi wewnętrznych, dashboardów, portali B2B i przepływów CRUD: odczyt danych, formularze, tabele, routing, authentication oraz authorization.

Refine zostawia Ci kontrolę nad warstwą UI. Możesz użyć Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS albo własnego design systemu. Możesz też pozostać w pełni headless z `@refinedev/core`.

## Dlaczego Refine?

- **Headless core:** zachowania związane z danymi, state i navigation są niezależne od frameworka UI.
- **Architektura providerów:** `dataProvider`, `authProvider`, `accessControlProvider`, `notificationProvider`, `i18nProvider` i router provider sprawiają, że integracje aplikacji można wymieniać.
- **Produktywność CRUD:** dostarcza wspólne wzorce dla operacji takich jak `list`, `show`, `create`, `edit` i `clone`.
- **Realne scenariusze:** obsługuje filtering, pagination, optimistic updates, realtime, audit logs oraz multi-tenancy.

## Podstawowa struktura

Aplikacje Refine są zwykle modelowane wokół `resources` i `providers`. `resources` opisują encje domeny, a `providers` łączą aplikację z danymi, uwierzytelnianiem, powiadomieniami i routingiem.

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

## Następne kroki

Aby utworzyć nowy projekt, przejdź do [Quickstart](/core/docs/getting-started/quickstart/). Aby lepiej zrozumieć architekturę, zacznij od [General Concepts](/core/docs/guides-concepts/general-concepts/) i [Data Fetching](/core/docs/guides-concepts/data-fetching/).
