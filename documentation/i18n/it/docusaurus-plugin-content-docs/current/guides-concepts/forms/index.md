---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Scopri come Refine aiuta a creare form create ed edit collegati al data provider."
---

In Refine i forms collegano l'input dell'utente alle mutation sui dati. Refine offre hooks e integrazioni UI affinché le pagine `create` ed `edit` gestiscano loading, validation, submit e redirect con pattern coerenti.

## Form hooks

Hooks come `useForm` preparano dati iniziali, submit handler e mutation state. Le integrazioni UI ufficiali mappano poi il risultato del hook sui componenti form di Ant Design, Material UI, Mantine, React Hook Form o altre librerie.

```tsx title=CreatePost.tsx
import { useForm } from "@refinedev/react-hook-form";

export const CreatePost = () => {
  const { refineCore, register, handleSubmit } = useForm();

  return (
    <form onSubmit={handleSubmit(refineCore.onFinish)}>
      <input {...register("title")} />
      <button type="submit">Save</button>
    </form>
  );
};
```

## Create ed edit

In una pagina `create`, il form in genere chiama `create` sul data provider. In una pagina `edit`, il form legge prima il record esistente e poi chiama `update` al submit.

## Mutation mode

Refine supporta mutation mode come `pessimistic`, `optimistic` e `undoable`. La scelta determina quando la UI viene aggiornata e se l'utente può annullare le modifiche.

## Validation

La validation può essere gestita con la libreria form scelta o tramite backend. Refine non impone una strategia: puoi usare schema validation, regole del framework UI o error response dell'API.

## Navigation dopo il submit

Dopo un submit riuscito, Refine può reindirizzare alla pagina `list`, `show`, `edit` o a un'altra route richiesta dal workflow.
