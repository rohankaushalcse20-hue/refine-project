# Refine için Supabase entegrasyonu

`@refinedev/supabase`, Refine uygulamalarını [Supabase](https://supabase.com/) projeleriyle bağlar. Data provider ve live provider ile Supabase tabloları üzerinde CRUD ve realtime workflow'ları kurmanıza yardımcı olur.

## Kurulum

```sh
npm install @refinedev/supabase
```

## Temel kullanım

```tsx
import { dataProvider, liveProvider, createClient } from "@refinedev/supabase";

const supabaseClient = createClient("SUPABASE_URL", "SUPABASE_KEY");

const App = () => {
  return (
    <Refine
      dataProvider={dataProvider(supabaseClient)}
      liveProvider={liveProvider(supabaseClient)}
    >
      {/* ... */}
    </Refine>
  );
};
```

## Dokümantasyon

- [Refine data provider dokümantasyonunu](https://refine.dev/docs/core/providers/data-provider) okuyun.
- [Supabase data provider dokümantasyonunu](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction) inceleyin.
- [Supabase resmi Refine tutorial'ını](https://supabase.com/docs/guides/getting-started/tutorials/with-refine) okuyun.
