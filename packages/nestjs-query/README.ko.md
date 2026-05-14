# NestJS Query data provider integration for refine

`@refinedev/nestjs-query`는 NestJS Query GraphQL APIs를 위한 data provider와 live provider를 제공합니다. GraphQL client와 subscription transport를 Refine의 CRUD 및 realtime workflows에 연결합니다.

## 설치

```sh
npm install @refinedev/nestjs-query graphql-tag graphql-ws
```

## 기본 사용법

```tsx
import dataProvider, {
  GraphQLClient,
  liveProvider,
} from "@refinedev/nestjs-query";

import { createClient } from "graphql-ws";

const App = () => (
  <Refine
    dataProvider={dataProvider(new GraphQLClient("API_URL"))}
    liveProvider={liveProvider(createClient({ url: "WS_URL" }))}
  >
    {/* ... */}
  </Refine>
);
```

NestJS Query schema와 GraphQL subscriptions를 사용하는 Refine app을 만들 때 이 integration이 유용합니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)과 [NestJS Query example](https://refine.dev/docs/examples/data-provider/nestjs-query/)을 참고하세요.
