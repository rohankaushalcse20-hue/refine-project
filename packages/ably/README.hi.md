# Ably integration for refine

`@refinedev/ably` Refine applications में realtime updates के लिए Ably-based live provider देता है। यह publish/subscribe messaging और WebSocket connections को Refine live provider contract से जोड़ता है।

## Installation

```sh
npm install @refinedev/ably
```

## Basic usage

```tsx
import { liveProvider, Ably } from "@refinedev/ably";

export const ablyClient = new Ably.Realtime("YOUR_API_TOKEN");

const App = () => (
  <Refine liveProvider={liveProvider(ablyClient)}>
    {/* ... */}
  </Refine>
);
```

जब records में realtime changes, collaborative screens या live dashboards दिखाने हों, तब यह package उपयोगी है।

Documentation के लिए [live provider docs](https://refine.dev/docs/api-references/providers/live-provider/) और [Ably tutorial](https://ably.com/tutorials/react-admin-panel-with-ably-and-refine) देखें।
