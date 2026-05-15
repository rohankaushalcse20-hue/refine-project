# Integrazione Ant Design per Refine

`@refinedev/antd` integra [Ant Design](https://ant.design/) con refine e fornisce componenti, layout, notifiche e helper pronti per costruire pannelli admin e dashboard.

## Installazione

```sh
npm install @refinedev/antd antd
```

## Uso di base

Importa gli elementi UI da `@refinedev/antd` e collegali alla tua applicazione refine insieme al tema e agli stili di Ant Design.

```tsx
import { Refine } from "@refinedev/core";
import { notificationProvider, ThemedLayoutV2 } from "@refinedev/antd";
```

Il pacchetto mantiene la logica dati in `@refinedev/core` e aggiunge un livello UI coerente con Ant Design per liste, form, pulsanti e layout.

## Documentazione

- Consulta la [documentazione di Ant Design in refine](https://refine.dev/docs/ui-integrations/ant-design/introduction/).
- Per i componenti di base, consulta la [documentazione Ant Design](https://ant.design/components/overview/).
