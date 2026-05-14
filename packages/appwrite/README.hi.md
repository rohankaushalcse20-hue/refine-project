# Appwrite integration for refine

`@refinedev/appwrite` Appwrite backends के लिए data provider और live provider देता है। इससे Appwrite databases और realtime capabilities को Refine resources से जोड़ा जा सकता है।

## Installation

```sh
npm install @refinedev/appwrite
```

## Basic usage

```tsx
import { dataProvider, liveProvider, Appwrite } from "@refinedev/appwrite";

const appwriteClient = new Appwrite();
appwriteClient.setEndpoint("API_URL").setProject("PROJECT_ID");

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, {
      databaseId: "default",
    })}
    liveProvider={liveProvider(appwriteClient, {
      databaseId: "default",
    })}
  >
    {/* ... */}
  </Refine>
);
```

Appwrite collections और realtime updates के ऊपर dashboards या admin screens बनाते समय यह package उपयोगी है।

Documentation के लिए [Appwrite package docs](https://refine.dev/docs/packages/documentation/data-providers/appwrite/) और [data provider guide](https://refine.dev/docs/core/providers/data-provider) देखें।
