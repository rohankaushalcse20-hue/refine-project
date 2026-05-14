<div align="center">
<a href="https://refine.dev/core">
    <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

# Refine CORE

**Refine CORE** est un méta-framework React open source pour les applications web riches en CRUD : outils internes, panels d'administration, dashboards et applications B2B.

Son architecture headless sépare la logique métier de l'UI et du routing. Vous pouvez donc l'utiliser avec vos propres composants, Ant Design, Material UI, Mantine, Chakra UI, Tailwind CSS, Next.js, Remix ou React Router.

## Installation rapide

```sh
npm create refine-app@latest my-refine-app
```

## Exemple minimal

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/simple-rest";

export default function App() {
  return (
    <Refine
      dataProvider={dataProvider("https://api.fake-rest.refine.dev")}
      resources={[{ name: "products", list: "/products" }]}
    />
  );
}
```

## Points clés

- Hooks headless pour données, formulaires, tables, auth, routing, notifications et i18n.
- Providers remplaçables pour connecter Refine à vos APIs et règles métier.
- Intégrations prêtes pour REST, GraphQL, Supabase, Hasura, Strapi, Appwrite et d'autres backends.
- Compatible avec les stacks React modernes sans imposer de design system unique.

Consultez la [documentation Refine](https://refine.dev/core/docs/) pour les guides complets.
