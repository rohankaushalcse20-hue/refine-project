# Inferencer for refine

`@refinedev/inferencer`는 API 또는 resource structure를 바탕으로 list, show, edit, create views의 시작 코드를 생성합니다. 반복적인 CRUD page setup을 줄이고, 생성된 code를 나중에 쉽게 customize할 수 있게 하는 것이 목적입니다.

## 설치

```sh
npm install @refinedev/inferencer
```

## 기본 사용법

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => (
  <Refine>
    <AntdInferencer action="list" resource="posts" />
  </Refine>
);
```

새 resource를 위한 quick prototype이나 수정 가능한 starting point가 필요할 때 Inferencer를 사용하세요.

자세한 내용은 [Inferencer documentation](https://refine.dev/docs/packages/documentation/inferencer/)과 [tutorial section](https://refine.dev/docs/tutorial/getting-started/antd/generate-crud-pages/#inferencer)을 참고하세요.
