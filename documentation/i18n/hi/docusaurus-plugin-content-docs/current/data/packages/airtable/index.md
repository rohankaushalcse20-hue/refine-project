---
title: "Airtable integration guide | Refine v5"
display_title: "Airtable"
sidebar_label: "Airtable"
description: "Refine v5 में Airtable data provider, API token setup और basic usage को Hindi में समझें।"
source: https://github.com/refinedev/refine/tree/main/packages/airtable
swizzle: true
---

Refine, CRUD applications बनाने के लिए [Airtable](https://airtable.com/) जैसे spreadsheet-database hybrid के लिए data provider प्रदान करता है।

:::simple Good to know

- `@refinedev/airtable` requests authenticate करने के लिए API Tokens का उपयोग करता है। Airtable के personal access tokens अभी supported नहीं हैं।
- यह integration requests संभालने के लिए [Airtable.js](https://github.com/Airtable/airtable.js) का उपयोग करती है।
- Refine में data fetching के बारे में अधिक जानने के लिए [Data Fetching](/core/docs/guides-concepts/data-fetching/) guide देखें।

:::

## Installation

<InstallPackagesCommand args="@refinedev/airtable"/>

## Usage

सबसे पहले अपने Airtable account से `API_TOKEN` और `BASE_ID` प्राप्त करें। फिर इन values को `dataProvider` function में pass करें।

```tsx title="app.tsx"
import Refine from "@refinedev/core";
import dataProvider from "@refinedev/airtable";

const App = () => (
  <Refine
    // highlight-next-line
    dataProvider={dataProvider("<API_TOKEN>", "<BASE_ID>")}
  >
    {/* ... */}
  </Refine>
);
```

## Example

<CodeSandboxExample path="data-provider-airtable" />
