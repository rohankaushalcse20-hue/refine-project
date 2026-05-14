# Medusa store integration for refine

`@refinedev/medusa`는 Medusa commerce backends를 위한 data provider와 auth helper를 제공합니다. Refine applications에서 products, orders, commerce workflows를 Medusa API와 연결할 수 있습니다.

## 설치

```sh
npm install @refinedev/medusa
```

## 기본 사용법

```tsx
import dataProvider, { authProvider } from "@refinedev/medusa";

const App = () => (
  <Refine
    dataProvider={dataProvider("API_URL")}
    authProvider={authProvider("API_URL")}
  >
    {/* ... */}
  </Refine>
);
```

Medusa store operations 위에 admin 또는 internal commerce tooling을 만들 때 이 package가 적합합니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)을 참고하세요.
