# Ably integration for refine

`@refinedev/ably` は、Ably を Refine の live provider として利用するための package です。WebSocket ベースの publish/subscribe 更新を Refine resource に接続し、リアルタイムな画面更新を実装できます。

## インストール

```sh
npm install @refinedev/ably
```

## 基本的な使い方

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => {
  return (
    <Refine liveProvider={liveProvider(ablyClient)}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

複数ユーザーが同じ resource を扱う管理画面で、作成、更新、削除などの変更をリアルタイムに反映したい場合に適しています。

## 詳細

- [refine live provider documentation](https://refine.dev/docs/api-references/providers/live-provider/)
- [Refine and Ably tutorial](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine)
- [refine documentation](https://refine.dev/docs/)
