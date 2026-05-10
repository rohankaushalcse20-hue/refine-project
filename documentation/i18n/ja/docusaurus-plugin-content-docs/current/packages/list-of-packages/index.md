---
title: "利用できるパッケージガイド | Refine v5 のパッケージ"
display_title: "パッケージ一覧"
sidebar_label: "パッケージ一覧"
description: "Refine v5 の core、UI、data providers、routing、realtime、コミュニティ統合向け主要パッケージを確認します。"
---

- `@refinedev/core` - **認証**、**アクセス制御**、**routing**、**networking**、**状態管理**、**i18n** のための `hooks`、`components`、`providers` をまとめたパッケージです。headless プロジェクトの出発点になります。
- `@refinedev/inferencer` - データ構造をもとに resources の views を自動生成できます。生成したコードはあとから簡単にカスタマイズできます。
- `@refinedev/cli` - refine の開発中によく使うコマンドを実行しやすくするツールです。

### UI framework 向けパッケージ

UI ライブラリとその統合について詳しく知りたい場合は、[UI Libraries](/core/docs/guides-concepts/ui-libraries/) ガイドを参照してください。

- [`@refinedev/antd`](/core/docs/ui-integrations/ant-design/introduction/) - [Ant Design](https://ant.design/) 向けサポート。Table、Form、Select、Menu、Layout、Notification、CRUD components など、framework 固有の `hooks` と `components` を **20+** 含みます。
- [`@refinedev/mui`](/core/docs/ui-integrations/material-ui/introduction/) - [Material UI](https://mui.com/material-ui/getting-started/overview/) 向けサポート。DataGrid (+ Pro)、AutoComplete、Menu、Layout、Notification、CRUD components など、framework 固有の `hooks` と `components` を **20+** 含みます。
- [`@refinedev/mantine`](/core/docs/ui-integrations/mantine/introduction/) - [Mantine](https://mantine.dev/) 向けサポート。Table、Form、AutoComplete、Menu、Layout、Notification、CRUD components など、framework 固有の `hooks` と `components` を **20+** 含みます。
- [`@refinedev/chakra-ui`](/core/docs/ui-integrations/chakra-ui/introduction/) - [Chakra UI](https://chakra-ui.com/) 向けサポート。Menu、Layout、Notification、CRUD components など、framework 固有の `components` を **20+** 含みます。
- [`@ferdiunal/refine-shadcn`](https://github.com/ferdiunal/refine-shadcn) - Refine と統合された ShadCN UI components。

### Data provider 向けパッケージ

Data providers について詳しくは、[Data Provider](/core/docs/data/data-provider/) ドキュメントを参照してください。

- [`@refinedev/simple-rest`](/core/docs/data/packages/simple-rest/) - 任意の **REST API** backend に接続します。
- [`@refinedev/graphql`](/core/docs/data/packages/graphql/) - 任意の **GraphQL** backend に接続します。
- [`@refinedev/nestjsx-crud`](/core/docs/data/packages/nestjsx-crud/) - **NestJs** で構築された **REST API** を利用します。
- [`@refinedev/nestjs-query`](/core/docs/data/packages/nestjs-query/) - **Nestjs-Query** で構築された **GraphQL API** を利用します。
- [`@refinedev/strapi-v4`](/core/docs/data/packages/strapi-v4/) - **REST API v4** 向けの [Strapi](https://strapi.io/) コネクタです。
- [`@refinedev/strapi`](/core/docs/data/packages/strapi-v4/) - 旧式の **REST API** 向けの [Strapi](https://strapi.io/) コネクタです。
- [`@refinedev/supabase`](/core/docs/data/packages/supabase/) - [Supabase](https://supabase.com/) の data provider。**live/realtime** プロジェクト向けに **Supabase Realtime** もサポートします。
- [`@refinedev/hasura`](/core/docs/data/packages/hasura/) - [Hasura GraphQL](https://hasura.io/) の data provider。**live/realtime** プロジェクト向けに **GraphQL Subscriptions** をサポートします。
- [`@refinedev/appwrite`](/core/docs/data/packages/appwrite/) - [Appwrite](https://appwrite.io/) の data provider。**live/realtime** プロジェクト向けに **Appwrite Realtime** をサポートします。
- [`@refinedev/airtable`](/core/docs/data/packages/airtable/) - [Airtable](https://airtable.com/) を backend サービスとして利用します。
- `@refinedev/medusa` - e-commerce プロジェクト向けの [Medusa](https://medusajs.com/) コネクタです。

### Router provider 向けパッケージ

Router providers について詳しくは、[Routing](/core/docs/guides-concepts/routing/) ガイドを参照してください。

- [`@refinedev/react-router`](/core/docs/routing/integrations/react-router/) - [React Router](https://reactrouter.com) 向け Router Provider
- [`@refinedev/nextjs-router`](/core/docs/routing/integrations/next-js/) - [Next.js](https://nextjs.org/docs/api-reference/next/router#userouter) 向け Router Provider
- [`@refinedev/remix-router`](/core/docs/routing/integrations/remix/) - [Remix](https://remix.run/) 向け Router Provider
- [`@refinenative/expo-router`](https://www.npmjs.com/package/@refinenative/expo-router) - [Expo](https://docs.expo.dev/) 向け Router Provider

### Live provider 向けパッケージ

Live providers について詳しくは、[Realtime](/core/docs/guides-concepts/realtime/) ガイドを参照してください。

- `@refinedev/ably` - realtime アプリケーション向けの [Ably](https://ably.com/) 統合です。
- `@refinedev/graphql` - GraphQL Subscriptions による realtime サポートです。
- `@refinedev/nestjs-query` - **Nestjs-Query** 向け GraphQL Subscriptions による realtime サポートです。
- `@refinedev/supabase` - [Supabase](https://supabase.com/) の realtime サポートです。
- `@refinedev/hasura` - GraphQL Subscriptions を使った [Hasura GraphQL](https://hasura.io/) のサポートです。
- `@refinedev/appwrite` - [Appwrite](https://appwrite.io/) の realtime サポートです。

### Integrations

- [`@refinedev/kbar`](/core/docs/packages/command-palette/) - [kbar](https://kbar.vercel.app/) との統合です。`command` / `ctrl` + `k` インターフェースをプロジェクトに追加できます。
- [`@refinedev/react-table`](/core/docs/packages/tanstack-table/introduction/) - [React Table](https://tanstack.com/table/v8) との統合です。headless プロジェクト向けの高機能な tables と datagrids を提供します。
- [`@refinedev/react-hook-form`](/core/docs/packages/react-hook-form/introduction/) - [React Hook Form](https://react-hook-form.com/) との統合です。拡張しやすいフォームとバリデーションを提供します。

### React frameworks

- `NextJS` - SSR と SSG のサポート
- `Remix` - SSR のサポート
- `React Native` - モバイル向けサポート

### ❤️ コミュニティパッケージ

- [`refine-firebase`](https://github.com/resulturan/refine-firebase) - [Firebase](https://firebase.google.com/) サービスのサポート
- [`@tspvivek/refine-directus`](https://github.com/tspvivek/refine-directus) - [Directus](https://directus.io/) で構築した backend 向けコネクタ
- [`refine-elide-rest`](https://github.com/chirdeeptomar/refine-elide-rest) - [Elide](https://elide.io/) で構築した backend 向けコネクタ
- [`refine-elide-graphql`](https://github.com/chirdeeptomar/refine-elide-graphql) - [Elide](https://elide.io/) で構築した GraphQL backend 向けコネクタ
- [`ent-refine`](https://github.com/diazoxide/entrefine) - [Entgo ORM](https://entgo.io/) と [GraphQL API](https://graphql.org/) をもとに [Refine](https://github.com/refinedev/refine) 向けの高いカスタマイズ性を持つ UI を生成するライブラリ
- [`refine-use-generated`](https://github.com/usegen/refine-use-generated) - [useGenerated](https://usegenerated.com/) で構築した GraphQL backend 向けコネクタ
- [`refine-hygraph`](https://github.com/acomagu/refine-hygraph) - [Hygraph](https://hygraph.com/) backend（GraphQL）向けコネクタ
- [`refine-sanity`](https://github.com/hirenf14/refine-sanity) - [Sanity](https://www.sanity.io/) backend 向けコネクタ
- [`refine-sqlite`](https://github.com/mateusabelli/refine-sqlite) - [SQLite](https://www.sqlite.org/index.html) backend 向けコネクタ
- [`refine-jsonapi`](https://github.com/MahirMahdi/refine-jsonapi) - [JSON:API](https://jsonapi.org/) backend 向けコネクタ
- [`@refine-auth/kinde-react`](https://github.com/hirenf14/refine-auth-kinde-react) - [Kinde](https://kinde.com) 認証のサポート
- [`refine-pocketbase`](https://github.com/kruschid/refine-pocketbase) - [PocketBase](https://pocketbase.io/) で構築した backend 向けコネクタ。auth provider と live provider もサポートします。
- [`refine-postgrest-ts`](https://github.com/ffimnsr/refine-postgrest-ts) - [PostgREST](https://postgrest.org) backend 向けコネクタ
- [`refine-chakra-ui-v3-ts`](https://github.com/ffimnsr/refine-chakra-ui-v3-ts) - [Chakra UI v3](https://www.chakra-ui.com) 向け統合
