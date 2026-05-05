---
title: "Autorisation | Refine v5"
display_title: "Autorisation"
sidebar_label: "Autorisation"
description: "Contrôlez les permissions et l'accès aux actions, routes et composants avec access control provider."
---

L'autorisation définit ce qu'un utilisateur authentifié peut faire. Refine la modélise avec un `accessControlProvider`, utilisable depuis hooks, boutons, menus et pages.

## Access control provider

La méthode principale est `can`. Elle reçoit le resource, l'action et des paramètres additionnels, puis renvoie si l'action est autorisée.

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

Utilisez `useCan` pour adapter l'interface, mais gardez toujours la validation finale côté backend.
