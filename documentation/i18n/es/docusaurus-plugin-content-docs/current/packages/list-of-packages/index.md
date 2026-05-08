---
title: "Guía de paquetes disponibles | Paquetes en Refine v5"
display_title: "Lista de paquetes"
sidebar_label: "Lista de paquetes"
description: "Consulta los paquetes principales de Refine v5 para core, UI, data providers, routing, realtime e integraciones comunitarias."
---

- `@refinedev/core` - Colección de `hooks`, `components` y `providers` para **autenticación**, **control de acceso**, **routing**, **networking**, **gestión de estado** e **i18n**. Es el punto de partida para proyectos headless.
- `@refinedev/inferencer` - Permite generar vistas para resources automáticamente a partir de la estructura de los datos. Su objetivo es reducir el tiempo dedicado a crear vistas generando código que luego puedes personalizar fácilmente.
- `@refinedev/cli` - Herramienta que te ayuda a ejecutar comandos importantes mientras desarrollas con refine.

### Paquetes de frameworks UI

Para conocer mejor las bibliotecas UI y sus integraciones, consulta la guía de [Bibliotecas UI](/core/docs/guides-concepts/ui-libraries/).

- [`@refinedev/antd`](/core/docs/ui-integrations/ant-design/introduction/) - Soporte para [Ant Design](https://ant.design/). Incluye **20+** `hooks` y `components` específicos del framework, como Table, Form, Select, Menu, Layout, Notification y componentes CRUD.
- [`@refinedev/mui`](/core/docs/ui-integrations/material-ui/introduction/) - Soporte para [Material UI](https://mui.com/material-ui/getting-started/overview/). Incluye **20+** `hooks` y `components` específicos del framework, como DataGrid (+ Pro), AutoComplete, Menu, Layout, Notification y componentes CRUD.
- [`@refinedev/mantine`](/core/docs/ui-integrations/mantine/introduction/) - Soporte para [Mantine](https://mantine.dev/). Incluye **20+** `hooks` y `components` específicos del framework, como Table, Form, AutoComplete, Menu, Layout, Notification y componentes CRUD.
- [`@refinedev/chakra-ui`](/core/docs/ui-integrations/chakra-ui/introduction/) - Soporte para [Chakra UI](https://chakra-ui.com/). Incluye **20+** `components` específicos del framework, como Menu, Layout, Notification y componentes CRUD.
- [`@ferdiunal/refine-shadcn`](https://github.com/ferdiunal/refine-shadcn) - Componentes de ShadCN UI integrados con Refine.

### Paquetes de data providers

Para aprender más sobre data providers, consulta la documentación de [Data Provider](/core/docs/data/data-provider/).

- [`@refinedev/simple-rest`](/core/docs/data/packages/simple-rest/) - Conecta cualquier backend **REST API** personalizado.
- [`@refinedev/graphql`](/core/docs/data/packages/graphql/) - Conecta cualquier backend **GraphQL** personalizado.
- [`@refinedev/nestjsx-crud`](/core/docs/data/packages/nestjsx-crud/) - Consume **REST API** creadas con **NestJs**.
- [`@refinedev/nestjs-query`](/core/docs/data/packages/nestjs-query/) - Consume **GraphQL API** creadas con **Nestjs-Query**.
- [`@refinedev/strapi-v4`](/core/docs/data/packages/strapi-v4/) - Conector de [Strapi](https://strapi.io/) para **REST API v4**.
- [`@refinedev/strapi`](/core/docs/data/packages/strapi-v4/) - Conector de [Strapi](https://strapi.io/) para **REST API legadas**.
- [`@refinedev/supabase`](/core/docs/data/packages/supabase/) - Data provider de [Supabase](https://supabase.com/). También soporta **Supabase Realtime** para proyectos **live/realtime**.
- [`@refinedev/hasura`](/core/docs/data/packages/hasura/) - Data provider de [Hasura GraphQL](https://hasura.io/). Soporta **GraphQL Subscriptions** para proyectos **live/realtime**.
- [`@refinedev/appwrite`](/core/docs/data/packages/appwrite/) - Data provider de [Appwrite](https://appwrite.io/). Soporta **Appwrite Realtime** para proyectos **live/realtime**.
- [`@refinedev/airtable`](/core/docs/data/packages/airtable/) - Usa [Airtable](https://airtable.com/) como servicio backend.
- `@refinedev/medusa` - Conector de [Medusa](https://medusajs.com/) para proyectos de e-commerce.

### Paquetes de router provider

Para aprender más sobre router providers, consulta la guía de [Routing](/core/docs/guides-concepts/routing/).

- [`@refinedev/react-router`](/core/docs/routing/integrations/react-router/) - Router Provider para [React Router](https://reactrouter.com)
- [`@refinedev/nextjs-router`](/core/docs/routing/integrations/next-js/) - Router Provider para [Next.js](https://nextjs.org/docs/api-reference/next/router#userouter)
- [`@refinedev/remix-router`](/core/docs/routing/integrations/remix/) - Router Provider para [Remix](https://remix.run/)
- [`@refinenative/expo-router`](https://www.npmjs.com/package/@refinenative/expo-router) - Router Provider para [Expo](https://docs.expo.dev/)

### Paquetes de live provider

Para aprender más sobre live providers, consulta la guía de [Realtime](/core/docs/guides-concepts/realtime/).

- `@refinedev/ably` - Integración de [Ably](https://ably.com/) para aplicaciones realtime.
- `@refinedev/graphql` - Soporte realtime mediante GraphQL Subscriptions.
- `@refinedev/nestjs-query` - Soporte realtime mediante GraphQL Subscriptions para **Nestjs-Query**.
- `@refinedev/supabase` - Soporte realtime de [Supabase](https://supabase.com/).
- `@refinedev/hasura` - Soporte de [Hasura GraphQL](https://hasura.io/) con GraphQL Subscriptions.
- `@refinedev/appwrite` - Soporte realtime de [Appwrite](https://appwrite.io/).

### Integraciones

- [`@refinedev/kbar`](/core/docs/packages/command-palette/) - Integración con [kbar](https://kbar.vercel.app/). Añade interfaces `command`/`crtrl`+`k` a tu proyecto.
- [`@refinedev/react-table`](/core/docs/packages/tanstack-table/introduction/) - Integración con [React Table](https://tanstack.com/table/v8). Tablas y datagrids potentes para proyectos headless.
- [`@refinedev/react-hook-form`](/core/docs/packages/react-hook-form/introduction/) - Integración con [React Hook Form](https://react-hook-form.com/). Formularios extensibles y validación para tus proyectos.

### Frameworks de React

- `NextJS` - Soporte SSR y SSG para tus proyectos.
- `Remix` - Soporte SSR para tus proyectos.
- `React Native` - Soporte móvil para tus proyectos.

### ❤️ Paquetes de la comunidad

- [`refine-firebase`](https://github.com/resulturan/refine-firebase) - Soporte para servicios de [Firebase](https://firebase.google.com/).
- [`@tspvivek/refine-directus`](https://github.com/tspvivek/refine-directus) - Conector para backends creados con [Directus](https://directus.io/)
- [`refine-elide-rest`](https://github.com/chirdeeptomar/refine-elide-rest) - Conector para backends creados con [Elide](https://elide.io/)
- [`refine-elide-graphql`](https://github.com/chirdeeptomar/refine-elide-graphql) - Conector para backends GraphQL creados con [Elide](https://elide.io/)
- [`ent-refine`](https://github.com/diazoxide/entrefine) - Librería que genera UI totalmente personalizable a partir de [Entgo ORM](https://entgo.io/) y [GraphQL API](https://graphql.org/) con [Refine](https://github.com/refinedev/refine)
- [`refine-use-generated`](https://github.com/usegen/refine-use-generated) - Conector para backends GraphQL creados con [useGenerated](https://usegenerated.com/)
- [`refine-hygraph`](https://github.com/acomagu/refine-hygraph) - Conector para backends de [Hygraph](https://hygraph.com/) (GraphQL)
- [`refine-sanity`](https://github.com/hirenf14/refine-sanity) - Conector para backends de [Sanity](https://www.sanity.io/)
- [`refine-sqlite`](https://github.com/mateusabelli/refine-sqlite) - Conector para backends de [SQLite](https://www.sqlite.org/index.html)
- [`refine-jsonapi`](https://github.com/MahirMahdi/refine-jsonapi) - Conector para backends [JSON:API](https://jsonapi.org/)
- [`@refine-auth/kinde-react`](https://github.com/hirenf14/refine-auth-kinde-react) - Soporte para autenticación con [Kinde](https://kinde.com).
- [`refine-pocketbase`](https://github.com/kruschid/refine-pocketbase) - Conector para backends creados con [PocketBase](https://pocketbase.io/). También soporta auth provider y live provider.
- [`refine-postgrest-ts`](https://github.com/ffimnsr/refine-postgrest-ts) - Conector para backends de [PostgREST](https://postgrest.org).
- [`refine-chakra-ui-v3-ts`](https://github.com/ffimnsr/refine-chakra-ui-v3-ts) - Integración para [Chakra UI v3](https://www.chakra-ui.com).
