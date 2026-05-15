# Refine için TanStack React Table entegrasyonu

`@refinedev/react-table`, Refine'ın data ve resource workflow'larını [TanStack React Table](https://tanstack.com/table/v8) ile bağlar. Headless table yapısını korurken filtering, sorting ve pagination gibi CRUD listeleme ihtiyaçlarını Refine hooks ile yönetmenizi sağlar.

## Kurulum

```sh
npm install @refinedev/react-table @tanstack/react-table
```

## Temel kullanım

```tsx
import { useTable } from "@refinedev/react-table";

const table = useTable({
  refineCoreProps: {
    resource: "posts",
  },
});
```

## Ne zaman kullanılır?

Kendi table markup ve stillerinizi korumak, ancak Refine'ın resource, filter ve query yönetiminden yararlanmak istediğinizde bu package'ı kullanın.

## Dokümantasyon

- [TanStack React Table ile Refine dokümantasyonunu](https://refine.dev/docs/packages/documentation/tanstack-table/introduction) okuyun.
- [Gelişmiş table örneğini](https://refine.dev/docs/examples/table/tanstack/advanced-react-table/) inceleyin.
