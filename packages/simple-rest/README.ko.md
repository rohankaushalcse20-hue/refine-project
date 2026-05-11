# Simple REST data provider

`@refinedev/simple-rest`는 구조가 일정한 REST API를 위한 data provider입니다. `json-server`와 비슷한 스타일을 기준으로 Refine의 resources를 HTTP endpoints에 연결합니다.

## 설치

```sh
npm install @refinedev/simple-rest
```

## 기본 사용법

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

backend가 목록 조회, 생성, 수정, 삭제를 위한 단순한 REST endpoints를 제공할 때 적합합니다. custom headers나 특별한 파라미터가 필요하면 wrapper를 만들어 확장해서 사용할 수 있습니다.
