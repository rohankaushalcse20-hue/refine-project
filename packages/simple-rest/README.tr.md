# Simple REST data provider

`@refinedev/simple-rest`, net yapılı REST APIs için bir data provider'dır. Refine içindeki `resources` yapılarını doğrudan HTTP endpoints ile bağlamak istediğinizde uygundur.

## Kurulum

```sh
npm install @refinedev/simple-rest
```

## Temel kullanım

```tsx
import dataProvider from "@refinedev/simple-rest";

const App = () => (
  <Refine dataProvider={dataProvider("API_URL")}>
    {/* ... */}
  </Refine>
);
```

Backend'iniz list, create, update ve delete işlemleri için standart endpoints sağlıyorsa bu provider iyi bir eşleşmedir. Özel headers veya params gerekiyorsa provider kolayca sarılıp genişletilebilir.
