---
title: "Packages की सूची | Refine v5"
display_title: "List of Packages"
sidebar_label: "List of Packages"
description: "Refine ecosystem के core, UI, data, router, realtime और community packages का Hindi अवलोकन।"
---

- `@refinedev/core` - **authentication**, **access control**, **routing**, **networking**, **state management** और **i18n** के लिए `hooks`, `components` और `providers` का संग्रह। Headless projects के लिए शुरुआती आधार।
- `@refinedev/inferencer` - resource data structure के आधार पर views generate करने में मदद करता है, ताकि आप generated code को customize करते हुए CRUD screens जल्दी बना सकें।
- `@refinedev/cli` - refine के साथ development करते समय जरूरी commands चलाने के लिए CLI tool।

### UI Framework Packages:

UI libraries और integrations के बारे में अधिक जानने के लिए [UI Libraries](/core/docs/guides-concepts/ui-libraries/) guide देखें।

- [`@refinedev/antd`](/core/docs/ui-integrations/ant-design/introduction/) - [Ant Design](https://ant.design/) support। **20+** framework-specific `hooks` और `components`, जिनमें Table, Form, Select, Menu, Layout, Notification और CRUD components शामिल हैं।
- [`@refinedev/mui`](/core/docs/ui-integrations/material-ui/introduction/) - [Material UI](https://mui.com/material-ui/getting-started/overview/) support। **20+** framework-specific `hooks` और `components`, जिनमें DataGrid (+ Pro), AutoComplete, Menu, Layout, Notification और CRUD components शामिल हैं।
- [`@refinedev/mantine`](/core/docs/ui-integrations/mantine/introduction/) - [Mantine](https://mantine.dev/) support। **20+** framework-specific `hooks` और `components`, जिनमें Table, Form, AutoComplete, Menu, Layout, Notification और CRUD components शामिल हैं।
- [`@refinedev/chakra-ui`](/core/docs/ui-integrations/chakra-ui/introduction/) - [Chakra UI](https://chakra-ui.com/) support। **20+** framework-specific `components`, जिनमें Menu, Layout, Notification और CRUD components शामिल हैं।
- [`@ferdiunal/refine-shadcn`](https://github.com/ferdiunal/refine-shadcn) - Refine के साथ ShadCN UI components।

### Data Provider Packages:

Data providers के बारे में अधिक जानने के लिए [Data Provider](/core/docs/data/data-provider/) docs देखें।

- [`@refinedev/simple-rest`](/core/docs/data/packages/simple-rest/) - किसी भी custom **REST API** backend से कनेक्ट करें।
- [`@refinedev/graphql`](/core/docs/data/packages/graphql/) - किसी भी custom **GraphQL** backend से कनेक्ट करें।
- [`@refinedev/nestjsx-crud`](/core/docs/data/packages/nestjsx-crud/) - **NestJs** से बनी **REST API** को consume करें।
- [`@refinedev/nestjs-query`](/core/docs/data/packages/nestjs-query/) - **Nestjs-Query** से बनी **GraphQL API** को consume करें।
- [`@refinedev/strapi-v4`](/core/docs/data/packages/strapi-v4/) - **v4 REST API** के लिए [Strapi](https://strapi.io/) connector।
- [`@refinedev/strapi`](/core/docs/data/packages/strapi-v4/) - legacy **REST API** के लिए [Strapi](https://strapi.io/) connector।
- [`@refinedev/supabase`](/core/docs/data/packages/supabase/) - [Supabase](https://supabase.com/) data provider। **live/realtime** projects के लिए Supabase Realtime support शामिल है।
- [`@refinedev/hasura`](/core/docs/data/packages/hasura/) - [Hasura GraphQL](https://hasura.io/) data provider। **live/realtime** projects के लिए GraphQL Subscriptions support शामिल है।
- [`@refinedev/appwrite`](/core/docs/data/packages/appwrite/) - [Appwrite](https://appwrite.io/) data provider। **live/realtime** projects के लिए Appwrite Realtime support शामिल है।
- [`@refinedev/airtable`](/core/docs/data/packages/airtable/) - [Airtable](https://airtable.com/) को backend service की तरह उपयोग करें।
- `@refinedev/medusa` - e-commerce projects के लिए [Medusa](https://medusajs.com/) connector।

### Router Provider Packages

Router providers के बारे में अधिक जानने के लिए [Routing](/core/docs/guides-concepts/routing/) guide देखें।

- [`@refinedev/react-router`](/core/docs/routing/integrations/react-router/) - [React Router](https://reactrouter.com) के लिए Router Provider।
- [`@refinedev/nextjs-router`](/core/docs/routing/integrations/next-js/) - [Next.js](https://nextjs.org/docs/api-reference/next/router#userouter) के लिए Router Provider।
- [`@refinedev/remix-router`](/core/docs/routing/integrations/remix/) - [Remix](https://remix.run/) के लिए Router Provider।
- [`@refinenative/expo-router`](https://www.npmjs.com/package/@refinenative/expo-router) - [Expo](https://docs.expo.dev/) के लिए Router Provider।

### Live Provider Packages

Live providers के बारे में अधिक जानने के लिए [Realtime](/core/docs/guides-concepts/realtime/) guide देखें।

- `@refinedev/ably` - realtime applications के लिए [Ably](https://ably.com/) integration।
- `@refinedev/graphql` - GraphQL Subscriptions के जरिए realtime support।
- `@refinedev/nestjs-query` - **Nestjs-Query** के लिए GraphQL Subscriptions आधारित realtime support।
- `@refinedev/supabase` - [Supabase](https://supabase.com/) realtime support।
- `@refinedev/hasura` - [Hasura GraphQL](https://hasura.io/) के लिए GraphQL Subscriptions support।
- `@refinedev/appwrite` - [Appwrite](https://appwrite.io/) realtime support।

### Integrations

- [`@refinedev/kbar`](/core/docs/packages/command-palette/) - [kbar](https://kbar.vercel.app/) integration। Project में `command`/`ctrl`+`k` interfaces जोड़ने के लिए।
- [`@refinedev/react-table`](/core/docs/packages/tanstack-table/introduction/) - [React Table](https://tanstack.com/table/v8) integration। Headless projects के लिए शक्तिशाली tables और datagrids।
- [`@refinedev/react-hook-form`](/core/docs/packages/react-hook-form/introduction/) - [React Hook Form](https://react-hook-form.com/) integration। Projects के लिए extensible forms और validation।

### React Frameworks

- `NextJS` - projects के लिए SSR और SSG support।
- `Remix` - projects के लिए SSR support।
- `React Native` - mobile support।

### ❤️ Community Packages:

- [`refine-firebase`](https://github.com/resulturan/refine-firebase) - [Firebase](https://firebase.google.com/) services के लिए support।
- [`@tspvivek/refine-directus`](https://github.com/tspvivek/refine-directus) - [Directus](https://directus.io/) पर बने backends के लिए connector।
- [`refine-elide-rest`](https://github.com/chirdeeptomar/refine-elide-rest) - [Elide](https://elide.io/) पर बने backends के लिए connector।
- [`refine-elide-graphql`](https://github.com/chirdeeptomar/refine-elide-graphql) - [Elide](https://elide.io/) पर बने GraphQL backends के लिए connector।
- [`ent-refine`](https://github.com/diazoxide/entrefine) - [Entgo ORM](https://entgo.io/) और [GraphQL API](https://graphql.org/) के साथ customizable UI generate करने वाली library।
- [`refine-use-generated`](https://github.com/usegen/refine-use-generated/) - [useGenerated](https://usegenerated.com/) पर बने GraphQL backends के लिए connector।
- [`refine-hygraph`](https://github.com/acomagu/refine-hygraph) - [Hygraph](https://hygraph.com/) backends (GraphQL) के लिए connector।
- [`refine-sanity`](https://github.com/hirenf14/refine-sanity) - [Sanity](https://www.sanity.io/) backends के लिए connector।
- [`refine-sqlite`](https://github.com/mateusabelli/refine-sqlite) - [SQLite](https://www.sqlite.org/index.html) backends के लिए connector।
- [`refine-jsonapi`](https://github.com/MahirMahdi/refine-jsonapi) - [JSON:API](https://jsonapi.org/) backends के लिए connector।
- [`@refine-auth/kinde-react`](https://github.com/hirenf14/refine-auth-kinde-react) - [Kinde](https://kinde.com) authentication support।
- [`refine-pocketbase`](https://github.com/kruschid/refine-pocketbase) - [PocketBase](https://pocketbase.io/) backends के लिए connector। Auth provider और live provider support भी उपलब्ध।
- [`refine-postgrest-ts`](https://github.com/ffimnsr/refine-postgrest-ts) - [PostgREST](https://postgrest.org) backends के लिए connector।
- [`refine-chakra-ui-v3-ts`](https://github.com/ffimnsr/refine-chakra-ui-v3-ts) - [Chakra UI v3](https://www.chakra-ui.com) integration।
