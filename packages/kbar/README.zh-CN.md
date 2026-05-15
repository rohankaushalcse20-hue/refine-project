# refine 的 kbar 集成

`@refinedev/kbar` 为 refine 应用添加基于 [kbar](https://kbar.vercel.app/) 的命令面板。它可以通过 command+k 风格的界面暴露导航和常用操作。

## 安装

```sh
npm install @refinedev/kbar
```

## 基本用法

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

当高级用户需要在仪表盘和内部工具中用更少点击完成导航与操作时，可以使用这个包。

## 文档

- 查看 refine 的 [command palette 示例](https://refine.dev/docs/examples/command-palette/)。
- 阅读 [refine 文档](https://refine.dev/docs/)。
