---
title: "Formulários | Refine v5"
display_title: "Formulários"
sidebar_label: "Formulários"
description: "Construa formulários de CRUD com Refine, integrações de UI e validação do servidor."
---

Formulários fazem parte de quase toda aplicação voltada ao usuário. O Refine oferece hooks e componentes que conectam campos, data providers, validação e mutações de forma consistente.

## Abordagem comum

Você pode usar Ant Design, Material UI, Mantine, Chakra UI ou React Hook Form. A lógica do Refine permanece separada da UI, então a biblioteca visual pode ser escolhida conforme o produto.

## Create e Edit

`useForm`, `useModalForm`, `useDrawerForm` e `useStepsForm` ajudam a implementar fluxos de criação, edição e formulários em etapas.

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Relacionamentos e validação

Com `useSelect`, você carrega opções de resources relacionados. Em aplicações multilíngues, vale combinar validação local, erros do servidor e mensagens traduzidas com i18n.
