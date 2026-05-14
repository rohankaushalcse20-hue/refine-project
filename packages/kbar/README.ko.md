# Command palette integration with kbar for refine

`@refinedev/kbar`는 Refine applications에 command palette를 추가하기 위한 integration을 제공합니다. kbar의 extensible command+k interface를 Refine resources와 application actions에 연결할 수 있습니다.

## 설치

```sh
npm install @refinedev/kbar
```

## 기본 사용법

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => (
  <RefineKbarProvider>
    <Refine>
      <RefineKbar />
    </Refine>
  </RefineKbarProvider>
);
```

navigation, resource actions, custom shortcuts를 빠르게 검색하고 실행하는 admin UI를 만들 때 유용합니다.

자세한 내용은 [refine kbar example](https://refine.dev/docs/examples/command-palette/)과 [Refine documentation](https://refine.dev/docs/)을 참고하세요.
