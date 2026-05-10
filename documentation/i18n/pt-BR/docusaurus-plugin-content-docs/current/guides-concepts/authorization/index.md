---
title: "Autorização | Refine v5"
display_title: "Autorização"
sidebar_label: "Autorização"
description: "Controle ações, rotas e componentes com o access control provider do Refine."
---

A autorização define o que um usuário autenticado pode fazer. No Refine, ela é modelada com `accessControlProvider` e pode ser aplicada em hooks, botões, menus e páginas.

## Access Control Provider

O método central é `can`. Ele recebe `resource`, `action` e, quando necessário, mais contexto para retornar a decisão de acesso.

```tsx
const accessControlProvider = {
  can: async ({ resource, action }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Only admins can delete posts" };
    }
    return { can: true };
  },
};
```

Com `useCan`, você adapta a UI às permissões disponíveis. Ainda assim, a verificação final de autorização deve continuar no backend.
