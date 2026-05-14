# Command palette integration with kbar for refine

`@refinedev/kbar` は、kbar を使った command palette を Refine アプリケーションに追加するための package です。resource への移動や主要な操作をキーボード中心で実行できるようにします。

## インストール

```sh
npm install @refinedev/kbar
```

## 基本的な使い方

```tsx
import { RefineKbar, RefineKbarProvider } from "@refinedev/kbar";

const App = () => {
  return (
    <RefineKbarProvider>
      <Refine>
        <RefineKbar />
      </Refine>
    </RefineKbarProvider>
  );
};
```

## 使いどころ

管理画面や内部ツールで、よく使うページ移動や操作を command palette から素早く実行したい場合に使います。

## 詳細

- [refine kbar example](https://refine.dev/docs/examples/command-palette/)
- [refine documentation](https://refine.dev/docs/)
- [refine tutorials](https://refine.dev/docs/tutorial/introduction/index/)
