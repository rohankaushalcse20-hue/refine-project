---
id: hasura
title: "Пример Hasura | Интеграция REST API в Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Внедрите Hasura в Refine v5. Изучите ключевые шаги. Освойте масштабирование REST и GraphQL для пользовательских API и масштабируемых потоков данных. Включены практические примеры."
example-tags: [data-provider, live-provider]
---

Любой пользовательский backend на REST или GraphQL можно интегрировать с Refine. Refine [Hasura](https://hasura.io/) GraphQL Data Provider доступен из коробки. Благодаря Refine можно подключиться к базе данных Hasura, создавать специальные запросы и удобно использовать данные. Этот пример подробно показывает, как работать с данными из базы Hasura в проекте Refine.

## Тип данных ID

По умолчанию data provider предполагает, что тип `ID` — `uuid`; это поведение можно изменить с помощью опции `idType`. В `idType` можно передать `Int` или `uuid`, либо использовать функцию, которая определяет `idType` на основе имени ресурса.

#### Передача 'Int' или 'uuid' в `idType`

Так можно задать `idType` для всех ресурсов.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Передача функции в `idType`

Так можно определять `idType` на основе имени ресурса.

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
