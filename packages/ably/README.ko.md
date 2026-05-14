# Ably integration for refine

`@refinedev/ably`는 Refine 애플리케이션에서 realtime updates를 처리하기 위한 Ably 기반 live provider를 제공합니다. publish/subscribe messaging과 WebSocket connections를 Refine의 live provider contract에 연결합니다.

## 설치

```sh
npm install @refinedev/ably
```

## 기본 사용법

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

records의 realtime changes, collaborative screens, live dashboards가 필요한 Refine 프로젝트에서 이 package를 사용하세요.

자세한 내용은 [live provider docs](https://refine.dev/docs/api-references/providers/live-provider/)와 [Ably tutorial](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine)을 참고하세요.
