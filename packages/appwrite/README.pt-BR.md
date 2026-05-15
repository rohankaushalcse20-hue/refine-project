# Integracao Appwrite para refine

`@refinedev/appwrite` fornece `dataProvider` e `liveProvider` para conectar aplicacoes refine ao [Appwrite](https://appwrite.io/). Ele e indicado para projetos que usam Appwrite como backend de dados, arquivos e eventos em tempo real.

## Instalacao

```sh
npm install @refinedev/appwrite
```

## Uso basico

```tsx
import { dataProvider, liveProvider, Appwrite } from "@refinedev/appwrite";

const appwriteClient = new Appwrite();
appwriteClient.setEndpoint("API_URL").setProject("PROJECT_ID");

const App = () => (
  <Refine
    dataProvider={dataProvider(appwriteClient, { databaseId: "default" })}
    liveProvider={liveProvider(appwriteClient, { databaseId: "default" })}
  >
    {/* ... */}
  </Refine>
);
```

## Documentacao

- Consulte a [documentacao de data provider do refine](https://refine.dev/docs/core/providers/data-provider).
- Leia a [documentacao Appwrite do refine](https://refine.dev/docs/packages/documentation/data-providers/appwrite/).
