# Supabase integration for refine

`@refinedev/supabase`는 Supabase projects를 위한 data provider와 live provider를 제공합니다. Supabase tables, auth context, realtime updates를 Refine resources에 연결할 수 있습니다.

## 설치

```sh
npm install @refinedev/supabase
```

## 기본 사용법

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

Supabase-backed admin panels, dashboards, internal tools를 만들 때 direct integration을 제공합니다.

자세한 내용은 [Supabase package docs](https://refine.dev/docs/packages/documentation/data-providers/supabase/#introduction), [Supabase guide](https://supabase.com/docs/guides/getting-started/tutorials/with-refine), [example](https://refine.dev/docs/examples/data-provider/supabase/)을 참고하세요.
