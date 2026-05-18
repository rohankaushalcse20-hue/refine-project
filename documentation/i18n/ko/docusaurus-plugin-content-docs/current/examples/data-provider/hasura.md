---
id: hasura
title: "Hasura 예제 | Refine v5 REST API Integration"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Refine v5에서 Hasura를 구현합니다. custom API와 확장 가능한 data flow를 위한 REST, GraphQL provider pattern을 hands-on example로 배웁니다."
example-tags: [data-provider, live-provider]
---

모든 REST 또는 GraphQL custom backend는 Refine와 통합해 사용할 수 있습니다. Refine [Hasura](https://hasura.io/) GraphQL Data Provider는 out-of-the-box로 제공됩니다. Refine 덕분에 Hasura database에 연결하고, 특별한 query를 만들고, data를 쉽게 사용할 수 있습니다. 이 예제는 Refine project에서 Hasura database의 data를 사용하는 방법을 자세히 보여 줍니다.

## ID Data Type

기본적으로 data provider는 `ID` type이 `uuid`라고 가정하지만, `idType` option을 사용해 이 동작을 변경할 수 있습니다. `idType` option 값으로 `Int` 또는 `uuid`를 전달하거나, resource name에 따라 `idType`을 결정하는 function을 사용할 수 있습니다.

#### `idType`에 'Int' 또는 'uuid' 전달하기

이렇게 하면 모든 resource의 `idType`을 결정할 수 있습니다.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### `idType`에 function 전달하기

이렇게 하면 resource name을 기준으로 `idType`을 결정할 수 있습니다.

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
