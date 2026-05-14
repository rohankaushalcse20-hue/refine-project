# Airtable integration for refine

`@refinedev/airtable` Airtable bases को Refine data provider के रूप में use करने देता है। इससे Airtable tables को resources की तरह expose करके admin panels और internal tools बनाए जा सकते हैं।

## Installation

```sh
npm install @refinedev/airtable
```

## Basic usage

```tsx
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine dataProvider={dataProvider("API_KEY", "BASE_ID")}>
    {/* ... */}
  </Refine>
);
```

Lightweight relational data को Airtable में रखते हुए Refine UI बनाना हो, तो यह provider fast starting point देता है।

अधिक जानकारी के लिए [data provider documentation](https://refine.dev/docs/core/providers/data-provider) और [Airtable example](https://refine.dev/docs/examples/data-provider/airtable/) देखें।
