---
id: hasura
title: "Contoh Hasura | Integrasi REST API di Refine v5"
display_title: "Hasura"
sidebar_label: "Hasura"
description: "Implementasikan Hasura di Refine v5. Pelajari langkah-langkah utamanya. Pelajari cara menskalakan REST dan GraphQL untuk API kustom serta alur data yang skalabel. Contoh langsung disertakan."
example-tags: [data-provider, live-provider]
---

Backend kustom REST atau GraphQL apa pun dapat diintegrasikan dengan Refine. Refine [Hasura](https://hasura.io/) GraphQL Data Provider tersedia langsung. Berkat Refine, Anda dapat terhubung ke database Hasura, membuat query khusus, dan menggunakan data dengan mudah. Contoh ini menunjukkan secara rinci cara menggunakan data di database Hasura Anda dengan proyek Refine.

## Tipe Data ID

Secara default, data provider menganggap tipe `ID` Anda adalah `uuid`; Anda dapat mengubah perilaku ini dengan menggunakan opsi `idType`. Anda dapat meneruskan `Int` atau `uuid` sebagai nilai opsi `idType`, atau menggunakan fungsi untuk menentukan `idType` berdasarkan nama resource.

#### Meneruskan 'Int' atau 'uuid' ke `idType`

Ini akan memungkinkan Anda menentukan `idType` untuk semua resource.

```tsx
const myDataProvider = dataProvider(client, {
  idType: "Int",
});
```

#### Meneruskan fungsi ke `idType`

Ini akan memungkinkan Anda menentukan `idType` berdasarkan nama resource.

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
