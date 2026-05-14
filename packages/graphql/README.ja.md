<div align="center" style="margin: 30px;">
    <a href="https://refine.dev">
    <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
    </a>
</div>

<br/>

<div align="center">
    <a href="https://refine.dev">ホームページ</a> |
    <a href="https://discord.gg/refine">Discord</a> |
    <a href="https://refine.dev/examples/">サンプル</a> |
    <a href="https://refine.dev/blog/">ブログ</a> |
    <a href="https://refine.dev/docs/">ドキュメント</a>

<br/>
<br/>

[![Discord](https://img.shields.io/discord/837692625737613362.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/refine)
[![Twitter Follow](https://img.shields.io/twitter/follow/refine_dev?style=social)](https://twitter.com/refine_dev)

<a href="https://www.producthunt.com/posts/refine-3?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-refine&#0045;3" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=362220&theme=light&period=daily" alt="refine - 100&#0037;&#0032;open&#0032;source&#0032;React&#0032;framework&#0032;to&#0032;build&#0032;web&#0032;apps&#0032;3x&#0032;faster | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

</div>

<br/>

<div align="center">refine は、エンタープライズ向けの内部ツール、管理画面、ダッシュボード、B2B アプリケーションを構築する開発者向けの、オープンソースでヘッドレスな React フレームワークです。

<br/>

CRUD 操作で繰り返し発生する作業を減らし、**authentication**、**access control**、**routing**、**networking**、**state management**、**i18n** など、重要なプロジェクト要素に業界標準の解決策を提供します。

</div>

# refine 向け GraphQL 統合

[GraphQL](https://graphql.org/) は、API のためのオープンソースのデータクエリおよび操作言語であり、クエリ実行エンジンです。

[refine](https://refine.dev/) は **headless by design** で、スタイリングとカスタマイズの自由度を高く保てます。利便性のために [Ant Design](https://ant.design/)、[Material UI](https://mui.com/material-ui/getting-started/overview/)、[Mantine](https://mantine.dev/)、[Chakra UI](https://chakra-ui.com/) とのすぐ使える統合も提供しています。

refine は REST API、[GraphQL](https://graphql.org/)、[Airtable](https://www.airtable.com/)、[Strapi](https://strapi.io/)、[Supabase](https://supabase.com/)、[Firebase](https://firebase.google.com/)、[NestJS](https://nestjs.com/) など、15 種類以上のバックエンドサービス向けコネクターを備えています。

## インストールと使い方

```
npm install @refinedev/graphql
```

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider(client)}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

## ドキュメント

- より詳しい情報と使い方は、[refine data provider documentation](https://refine.dev/docs/core/providers/data-provider) を参照してください。
- [refine GraphQL docs を参照してください](https://refine.dev/docs/packages/documentation/data-providers/graphql/)
- [refine の詳細はドキュメントを参照してください](https://refine.dev/docs/)
- [refine のチュートリアルへ進む](https://refine.dev/docs/tutorial/introduction/index/)
