# Hasura integration for refine

`@refinedev/hasura`는 Hasura-backed GraphQL APIs를 위한 data provider를 제공합니다. Hasura endpoints, headers, Refine resources를 연결해 admin panels와 internal tools에서 CRUD operations를 실행할 수 있게 합니다.

## 설치

```sh
npm install @refinedev/hasura
```

## 기본 사용법

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/hasura";

const client = new GraphQLClient("HASURA_API_URL", {
  headers: {
    "x-hasura-role": "public",
  },
});

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

Hasura authorization rules와 GraphQL schema 위에 Refine UI를 만들 때 이 provider가 유용합니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)을 참고하세요.
