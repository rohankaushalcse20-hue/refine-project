# Strapi v4 integration for refine

`@refinedev/strapi-v4` Strapi v4 APIs के लिए data provider और auth helper देता है। यह headless CMS content को Refine resources से जोड़कर CRUD screens बनाना आसान करता है।

## Installation

```sh
npm install @refinedev/strapi-v4 axios
```

## Basic usage

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

Strapi v4 collections, authentication और custom axios setup के साथ Refine app बनाते समय यह integration उपयोगी है।

Documentation के लिए [Strapi v4 data provider docs](https://refine.dev/docs/packages/documentation/data-providers/strapi-v4/) और [example](https://refine.dev/docs/examples/data-provider/strapi-v4/) देखें।
