# Inferencer

`@refinedev/inferencer` は、resource のデータ構造をもとに Refine の list、show、edit、create 画面の雛形を自動生成する package です。生成されたコードは確認しながらカスタマイズできるため、初期実装の時間を短縮できます。

## インストール

```sh
npm install @refinedev/inferencer
```

## 基本的な使い方

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";

const App = () => {
  return (
    <Refine>
      <AntdInferencer action="list" resource="posts" />
    </Refine>
  );
};
```

## 使いどころ

API の構造を確認しながら CRUD 画面を素早く試作したい場合や、UI 統合ごとの標準的な実装例を出発点にしたい場合に便利です。

## 詳細

- [refine Inferencer documentation](https://refine.dev/docs/packages/documentation/inferencer/)
- [Inferencer tutorial](https://refine.dev/docs/tutorial/getting-started/antd/generate-crud-pages/#inferencer)
- [refine documentation](https://refine.dev/docs/)
