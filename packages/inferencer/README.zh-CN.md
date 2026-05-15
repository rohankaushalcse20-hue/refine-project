# refine Inferencer

`@refinedev/inferencer` 会根据数据结构生成资源的初始页面。它的目标是加速 CRUD 页面创建，并交付一个之后仍可继续自定义的起点。

## 安装

```sh
npm install @refinedev/inferencer
```

## 基本用法

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => (
  <Refine>
    <AntdInferencer action="list" resource="posts" />
  </Refine>
);
```

可以用 Inferencer 快速探索 API、验证数据模型，并生成后续可手动细化的页面。

## 文档

- 查看 [Inferencer 文档](https://refine.dev/docs/packages/documentation/inferencer/)。
- 阅读教程中的 [Inferencer 章节](https://refine.dev/docs/tutorial/getting-started/antd/generate-crud-pages/#inferencer)。
