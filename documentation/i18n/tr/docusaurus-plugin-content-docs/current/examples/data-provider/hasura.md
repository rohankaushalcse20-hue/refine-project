---
id: hasura
title: "Hasura Örneği | Refine v5'te REST API Entegrasyonu"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Refine v5'te Hasura uygulayın. Temel adımları öğrenin. Özel API'ler ve ölçeklenebilir data flow'lar için REST ve GraphQL kullanımını pratik örneklerle inceleyin."
example-tags: [data-provider, live-provider]
---

Herhangi bir REST veya GraphQL özel backend Refine ile entegre çalışabilir. Refine [Hasura](https://hasura.io/) GraphQL Data Provider kullanıma hazır olarak gelir. Refine sayesinde Hasura database'inize bağlanabilir, özel sorgular oluşturabilir ve verinizi kolayca kullanabilirsiniz. Bu örnek, Hasura database'inizdeki verileri Refine projesiyle nasıl kullanabileceğinizi ayrıntılı şekilde gösterir.

## ID Data Type

Varsayılan olarak data provider, `ID` tipinizin `uuid` olduğunu varsayar. Bu davranışı `idType` seçeneğini kullanarak değiştirebilirsiniz. `idType` seçeneğine değer olarak `Int` veya `uuid` geçebilir ya da resource adına göre `idType` belirlemek için fonksiyon kullanabilirsiniz.

#### `idType` için 'Int' veya 'uuid' geçirmek

Bu, tüm resource'lar için `idType` değerini belirlemenizi sağlar.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### `idType` için fonksiyon geçirmek

Bu, resource adına göre `idType` değerini belirlemenizi sağlar.

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
