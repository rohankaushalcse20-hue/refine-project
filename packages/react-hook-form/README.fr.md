<div align="center" style="margin: 30px;">
    <a href="https://refine.dev">
    <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
    </a>
</div>

# Intégration React Hook Form pour Refine

`@refinedev/react-hook-form` relie les formulaires Refine à [React Hook Form](https://react-hook-form.com/). Il permet de gérer les champs, validations et mutations Refine sans perdre la flexibilité de React Hook Form.

## Installation

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Utilisation de base

```tsx
import { useForm } from "@refinedev/react-hook-form";

const EditPost = () => {
  const { register, handleSubmit, formState, refineCore } = useForm({
    refineCoreProps: {
      resource: "posts",
      id: "1",
    },
  });

  return; /* ... */
};
```

## À retenir

- `refineCoreProps` transmet `resource`, `id`, `action` et options de mutation à Refine.
- React Hook Form garde la gestion fine des champs et de la validation.
- L'intégration fonctionne avec les data providers, notifications et redirections Refine.

Consultez la documentation Refine pour les usages avancés de `useForm`, `useModalForm` et `useStepsForm`.
