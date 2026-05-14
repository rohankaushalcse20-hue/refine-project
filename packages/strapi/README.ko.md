# Strapi integration for refine

`@refinedev/strapi`는 Strapi APIs를 위한 data provider와 auth helper를 제공합니다. headless CMS content types를 Refine resources처럼 사용할 수 있게 돕습니다.

## 설치

```sh
npm install @refinedev/strapi axios
```

## 기본 사용법

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi";

const axiosInstance = axios.create();
const strapiAuthHelper = AuthHelper("API_URL");

const App = () => (
  <Refine dataProvider={DataProvider("API_URL", axiosInstance)}>
    {/* ... */}
  </Refine>
);
```

Strapi content, permissions, custom axios configuration과 함께 Refine admin UI를 만들 때 이 integration이 적합합니다.

자세한 내용은 [data provider documentation](https://refine.dev/docs/core/providers/data-provider)과 [Strapi example](https://refine.dev/docs/examples/data-provider/strapi/)을 참고하세요.
