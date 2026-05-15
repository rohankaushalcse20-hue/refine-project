# Integracion de Supabase para Refine

`@refinedev/supabase` conecta Refine con [Supabase](https://supabase.com/). Proporciona data provider y live provider para crear herramientas internas sobre Postgres, autenticacion y realtime de Supabase.

## Instalacion

```sh
npm install @refinedev/supabase
```

## Uso basico

```tsx
import { dataProvider, liveProvider, createClient } from "@refinedev/supabase";

const supabaseClient = createClient("SUPABASE_URL", "SUPABASE_KEY");

const App = () => (
  <Refine
    dataProvider={dataProvider(supabaseClient)}
    liveProvider={liveProvider(supabaseClient)}
  >
    {/* ... */}
  </Refine>
);
```

## Documentacion

Consulta la [documentacion de data providers de Refine](https://refine.dev/docs/data/data-provider/) y la documentacion de Supabase para ajustar permisos, tablas y realtime.
