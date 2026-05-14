# NestJSX CRUD data provider integration for refine

`@refinedev/nestjsx-crud`는 NestJSX CRUD style REST APIs를 위한 data provider를 제공합니다. NestJS-based endpoints를 Refine resources와 CRUD hooks에 연결합니다.

## 설치

```sh
npm install @refinedev/nestjsx-crud
```

## 기본 사용법

```tsx
import dataProvider from "@refinedev/nestjsx-crud";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

API가 NestJSX CRUD conventions를 따를 때 request mapping과 handling을 단순하게 유지할 수 있습니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)과 [NestJS CRUD example](https://refine.dev/docs/examples/data-provider/nestjsxCrud/)을 참고하세요.
