# GraphQL integration for refine

`@refinedev/graphql`은 GraphQL APIs를 위한 data provider를 제공합니다. Refine resources를 GraphQL queries와 mutations에 연결해 list, create, update, delete workflows가 standard data provider contract로 동작하도록 돕습니다.

## 설치

```sh
npm install @refinedev/graphql
```

## 기본 사용법

```tsx
import dataProvider, { GraphQLClient } from "@refinedev/graphql";

const client = new GraphQLClient("YOUR_API_URL");

const App = () => (
  <Refine dataProvider={dataProvider(client)}>
    {/* ... */}
  </Refine>
);
```

backend가 GraphQL schema를 expose하고 Refine hooks로 동일한 CRUD flow를 유지하고 싶을 때 적합합니다.

문서는 [data provider guide](https://refine.dev/docs/core/providers/data-provider)와 [GraphQL package docs](https://refine.dev/docs/packages/documentation/data-providers/graphql/)를 참고하세요.
