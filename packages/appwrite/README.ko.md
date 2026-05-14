# Appwrite integration for refine

`@refinedev/appwrite`는 Appwrite backends를 위한 data provider와 live provider를 제공합니다. Appwrite databases와 realtime capabilities를 Refine resources에 연결할 수 있습니다.

## 설치

```sh
npm install @refinedev/appwrite
```

## 기본 사용법

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

Appwrite collections와 realtime updates 위에 dashboards나 admin screens를 만들 때 이 package가 유용합니다.

자세한 내용은 [Appwrite package docs](https://refine.dev/docs/packages/documentation/data-providers/appwrite/)와 [data provider guide](https://refine.dev/docs/core/providers/data-provider)를 참고하세요.
