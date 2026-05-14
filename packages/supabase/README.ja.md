# Supabase integration for refine

`@refinedev/supabase` は、Supabase を Refine の data provider と live provider として利用するための package です。Postgres ベースのデータ操作と realtime 更新を Refine resource に接続できます。

## インストール

```sh
npm install @refinedev/supabase
```

## 基本的な使い方

```tsx
import { dataProvider, liveProvider, createClient } from "@refinedev/supabase";

const supabaseClient = createClient("SUPABASE_URL", "SUPABASE_KEY");

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider(supabaseClient)}
      liveProvider={liveProvider(supabaseClient)}
    >
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

Supabase の database、認証、realtime 機能を使い、Refine で管理画面や内部ツールを構築したい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine Supabase docs](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction)
- [refine Supabase data provider example](https://refine.dev/docs/examples/data-provider/supabase/)
