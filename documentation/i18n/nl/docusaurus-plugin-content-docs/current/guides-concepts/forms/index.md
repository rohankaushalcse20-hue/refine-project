---
title: "Forms | Refine v5"
display_title: "Forms"
sidebar_label: "Forms"
description: "Bouw create- en edit-formulieren met Refine hooks en je favoriete formulierbibliotheek."
displayed_sidebar: mainSidebar
slug: /guides-concepts/forms
---

Formulieren in Refine combineren provideracties met formulierstate. Je kunt headless werken met core hooks of UI-integraties gebruiken voor Ant Design, Material UI, Mantine, Chakra UI en React Hook Form.

## Create en edit

Create-pagina's sturen data meestal naar `create`; edit-pagina's laden eerst een record en sturen wijzigingen naar `update`. Refine abstraheert deze flow zodat je formulier vooral velden, validatie en layout bevat.

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Server-side validatie

Wanneer de backend validatiefouten terugstuurt, kun je die vertalen naar veldfouten in je formulierbibliotheek. Zo blijft de bron van waarheid bij de API, terwijl gebruikers direct zien wat ze moeten aanpassen.

## Relaties en selectvelden

Hooks zoals `useSelect` helpen bij relationele velden. Ze halen opties op via de `dataProvider` en kunnen filters of sorters gebruiken om de keuzelijst te beperken.

## Gebruikerservaring

Gebruik loading states, disabled save buttons en duidelijke notificaties rond mutaties. Voor langere formulieren kan een patroon zoals save-and-continue nuttig zijn.
