# Integrazione Hasura per refine

`@refinedev/hasura` collega refine a [Hasura](https://hasura.io/) e alle API GraphQL generate sui tuoi dati.

## Installazione

```sh
npm install @refinedev/hasura graphql-ws
```

## Uso di base

Configura endpoint, headers e client GraphQL, quindi passa il data provider Hasura al componente `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/hasura";
```

Il provider è utile quando vuoi usare gli hooks CRUD di refine sopra uno schema Hasura con query, mutation e autorizzazioni gestite dal backend.

## Documentazione

- Consulta la [documentazione del provider Hasura](https://refine.dev/docs/data/packages/hasura/).
- Per configurare il backend, consulta la [documentazione Hasura](https://hasura.io/docs/latest/index/).
