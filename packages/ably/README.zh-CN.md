# refine 的 Ably 集成

`@refinedev/ably` 为 refine 应用提供基于 [Ably](https://ably.com/) 的 `liveProvider`。当内部工具、仪表盘或管理后台需要通过 WebSocket 接收实时更新时，可以使用这个包。

## 安装

```sh
npm install @refinedev/ably
```

## 基本用法

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

该 provider 会把 Ably 事件连接到 refine 的 realtime 契约，让数据事件逻辑与视觉层保持解耦。

## 文档

- 查看 refine 的 [live provider 文档](https://refine.dev/docs/api-references/providers/live-provider/)。
- 也可以阅读 Ably 官方的 [Ably 与 refine 教程](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine)。
