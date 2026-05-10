---
title: "i18n Provider | Refine v5"
display_title: "i18n Provider"
sidebar_label: "i18n Provider"
description: "Conecte sua biblioteca de tradução preferida ao Refine por meio de `i18nProvider`."
---

O Refine não impõe uma biblioteca específica de tradução. Em vez disso, ele trabalha com um `i18nProvider` que pode adaptar `react-i18next`, `next-i18next` ou uma solução interna.

## Interface mínima

```tsx
const i18nProvider = {
  translate: (key, options, defaultMessage) => defaultMessage ?? key,
  changeLocale: (lang) => Promise.resolve(lang),
  getLocale: () => "pt-BR",
};
```

Passe o provider para `<Refine />` para fornecer textos localizados a menus, botões e componentes.

```tsx
<Refine i18nProvider={i18nProvider}>{/* ... */}</Refine>
```

Para traduzir, trocar o idioma e ler o locale atual, use `useTranslate`, `useSetLocale` e `useGetLocale`.
