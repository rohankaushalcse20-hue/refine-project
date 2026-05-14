# Appwrite integration for refine

`@refinedev/appwrite` は、Appwrite backend 向けの data provider と live provider を提供します。Appwrite databases と realtime 機能を Refine resource に接続できます。

## インストール

```sh
npm install @refinedev/appwrite
```

## 基本的な使い方

```tsx
import { dataProvider, liveProvider, Appwrite } from "@refinedev/appwrite";

const appwriteClient = new Appwrite();
appwriteClient.setEndpoint("API_URL").setProject("PROJECT_ID");

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, {
      databaseId: "default",
    })}
    liveProvider={liveProvider(appwriteClient, {
      databaseId: "default",
    })}
  >
    {/* ... */}
  </Refine>
);
```

## 使いどころ

Appwrite collections と realtime updates を使って、dashboard、admin screen、内部ツールを Refine で構築したい場合に使います。

## 詳細

- [Appwrite package docs](https://refine.dev/docs/packages/documentation/data-providers/appwrite/)
- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine documentation](https://refine.dev/docs/)
