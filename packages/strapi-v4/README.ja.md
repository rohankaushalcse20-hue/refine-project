# Strapi v4 integration for refine

`@refinedev/strapi-v4` は、Strapi v4 backend を Refine の data provider として接続する package です。Strapi の content type を Refine の resource として扱い、CMS 管理画面や業務アプリケーションを構築できます。

## インストール

```sh
npm install @refinedev/strapi-v4 axios
```

## 基本的な使い方

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi-v4";

const axiosInstance = axios.create();
const strapiAuthHelper = AuthHelper("API_URL");

const App = () => {
  return (
    <Refine dataProvider={DataProvider("API_URL", axiosInstance)}>
      {/* ... */}
    </Refine>
  );
};
```

## 使いどころ

Strapi v4 の content API を使って、記事、商品、設定データなどを管理する Refine 画面を作りたい場合に適しています。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine StrapiV4 data provider docs](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/)
- [refine StrapiV4 data provider example](https://refine.dev/docs/examples/data-provider/strapi-v4/)
