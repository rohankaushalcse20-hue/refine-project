# Airtable integration for refine

`@refinedev/airtable`은 Airtable bases를 Refine data provider로 사용할 수 있게 해 줍니다. Airtable tables를 resources처럼 연결해 admin panels와 internal tools를 빠르게 만들 수 있습니다.

## 설치

```sh
npm install @refinedev/airtable
```

## 기본 사용법

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

가벼운 relational data를 Airtable에서 관리하면서 Refine UI를 구축해야 할 때 좋은 출발점입니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)와 [Airtable example](https://refine.dev/docs/examples/data-provider/airtable/)을 참고하세요.
