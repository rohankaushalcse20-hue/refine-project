# Strapi v4 integration for refine

`@refinedev/strapi-v4`는 Strapi v4 APIs를 위한 data provider와 auth helper를 제공합니다. headless CMS content를 Refine resources에 연결해 CRUD screens를 만들기 쉽게 합니다.

## 설치

```sh
npm install @refinedev/strapi-v4 axios
```

## 기본 사용법

```tsx
import { DataProvider, AuthHelper } from "@refinedev/strapi-v4";

const axiosInstance = axios.create();
const strapiAuthHelper = AuthHelper("API_URL");

const App = () => (
  <Refine dataProvider={DataProvider("API_URL", axiosInstance)}>
    {/* ... */}
  </Refine>
);
```

Strapi v4 collections, authentication, custom axios setup과 함께 Refine app을 만들 때 이 integration이 유용합니다.

자세한 내용은 [Strapi v4 data provider docs](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/)와 [example](https://refine.dev/docs/examples/data-provider/strapi-v4/)을 참고하세요.
