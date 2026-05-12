---
id: hasura
title: "Hasura example | Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Refine v5 में Hasura GraphQL data provider example, idType handling और query usage को Hindi में समझें।"
example-tags: [data-provider, live-provider]
---

Refine के साथ कोई भी custom REST या GraphQL backend जोड़ा जा सकता है। Refine का [Hasura](https://hasura.io/) GraphQL Data Provider built-in support देता है, जिससे आप Hasura database से कनेक्ट होकर custom queries बना सकते हैं और data को आसानी से उपयोग कर सकते हैं। यह example विस्तार से दिखाता है कि Refine project में Hasura data के साथ कैसे काम किया जाए।

## ID data type

Default रूप से data provider मानता है कि आपका `ID` type `uuid` है। आप `idType` option का उपयोग करके इस behavior को बदल सकते हैं। `idType` में सीधे `Int` या `uuid` दिया जा सकता है, या resource name के आधार पर value तय करने के लिए function का उपयोग किया जा सकता है।

#### `idType` में `Int` या `uuid` pass करना

इस तरीके से आप सभी resources के लिए `idType` निर्धारित कर सकते हैं।

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### `idType` में function pass करना

इस तरीके से आप resource name के आधार पर `idType` निर्धारित कर सकते हैं।

```tsx
const idTypeMap: Record<string, "Int" | "uuid"> = {
  users: "Int",
  posts: "uuid",
};

const myDataProvider = dataProvider(client, {
  idType: (resource) => idTypeMap[resource] ?? "uuid",
});
```

<CodeSandboxExample path="data-provider-hasura" />
