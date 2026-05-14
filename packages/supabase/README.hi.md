# Supabase integration for refine

`@refinedev/supabase` Supabase projects के लिए data provider और live provider देता है। इससे Supabase tables, auth context और realtime updates को Refine resources से जोड़ा जा सकता है।

## Installation

```sh
npm install @refinedev/supabase
```

## Basic usage

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

Supabase-backed admin panels, dashboards या internal tools बनाते समय यह package direct integration देता है।

अधिक जानकारी के लिए [Supabase package docs](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction), [Supabase guide](https://supabase.com/docs/guides/getting-started/tutorials/with-refine) और [example](https://refine.dev/docs/examples/data-provider/supabase/) देखें।
