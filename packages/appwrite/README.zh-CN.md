# refine 的 Appwrite 集成

`@refinedev/appwrite` 提供 `dataProvider` 和 `liveProvider`，用于把 refine 应用连接到 [Appwrite](https://appwrite.io/)。它适合使用 Appwrite 作为数据、文件和实时事件后端的项目。

## 安装

```sh
npm install @refinedev/appwrite
```

## 基本用法

```tsx
import { dataProvider, liveProvider, Appwrite } from "@refinedev/appwrite";

const appwriteClient = new Appwrite();
appwriteClient.setEndpoint("API_URL").setProject("PROJECT_ID");

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, { databaseId: "default" })}
    liveProvider={liveProvider(appwriteClient, { databaseId: "default" })}
  >
    {/* ... */}
  </Refine>
);
```

## 文档

- 查看 refine 的 [data provider 文档](https://refine.dev/docs/core/providers/data-provider)。
- 阅读 refine 的 [Appwrite 文档](https://refine.dev/docs/packages/documentation/data-providers/appwrite/)。
