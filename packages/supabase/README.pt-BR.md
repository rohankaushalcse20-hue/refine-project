# Integracao Supabase para refine

`@refinedev/supabase` conecta o Refine ao [Supabase](https://supabase.com/) usando data provider e live provider. Ele e util quando a aplicacao usa tabelas, autenticacao ou eventos em tempo real do Supabase.

## Instalacao

```sh
npm install @refinedev/supabase
```

## Uso basico

```tsx
import { dataProvider, liveProvider, createClient } from "@refinedev/supabase";

const supabaseClient = createClient("SUPABASE_URL", "SUPABASE_KEY");

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider(supabaseClient)}
      liveProvider={liveProvider(supabaseClient)}
      /* ... */
    >
      {/* ... */}
    </Refine>
  );
};
```

## Documentacao

- Consulte a [documentacao de data providers do refine](https://refine.dev/docs/core/providers/data-provider).
- Veja a [documentacao do Supabase provider](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction).
- Veja o [exemplo de data provider Supabase](https://refine.dev/docs/examples/data-provider/supabase/).
