# Strapi integration for refine

`@refinedev/strapi` は、Strapi backend を Refine の data provider として接続する package です。Strapi の content type を resource として扱い、CMS や管理画面の UI を Refine で構築できます。

## インストール

```sh
npm install @refinedev/strapi axios
```

## 基本的な使い方

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi";

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

Strapi を backend にしたコンテンツ管理、運用管理、ダッシュボードを、Refine の CRUD と認証の流れに合わせたい場合に使います。

## 詳細

- [refine data provider documentation](https://refine.dev/docs/core/providers/data-provider)
- [refine Strapi data provider example](https://refine.dev/docs/examples/data-provider/strapi/)
- [refine documentation](https://refine.dev/docs/)
