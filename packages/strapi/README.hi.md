# Strapi integration for refine

`@refinedev/strapi` Strapi APIs के लिए data provider और auth helper देता है। यह headless CMS content types को Refine resources की तरह इस्तेमाल करने में मदद करता है।

## Installation

```sh
npm install @refinedev/strapi axios
```

## Basic usage

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

Strapi content, permissions और custom axios configuration के साथ Refine admin UI बनाते समय यह integration उपयोगी है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) और [Strapi example](https://refine.dev/docs/examples/data-provider/strapi/) देखें।
