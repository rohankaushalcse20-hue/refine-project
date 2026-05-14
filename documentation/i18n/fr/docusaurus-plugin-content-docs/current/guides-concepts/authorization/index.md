---
title: "Autorisation | Refine v5"
display_title: "Autorisation"
sidebar_label: "Autorisation"
description: "Utilisez l'accessControlProvider pour contrôler les actions visibles et autorisées dans une application Refine."
---

L'autorisation détermine ce qu'un utilisateur authentifié peut faire. Dans Refine, cette logique est fournie par `accessControlProvider`.

## Access control provider

Le provider expose principalement une méthode `can`. Elle reçoit une `resource`, une `action`, des paramètres optionnels et retourne si l'action est autorisée.

```tsx
const accessControlProvider = {
  can: async ({ resource, action, params }) => {
    if (resource === "products" && action === "delete") {
      return { can: false, reason: "Unauthorized" };
    }

    return { can: true };
  },
};
```

Passez-le ensuite à `<Refine />` :

```tsx
<Refine accessControlProvider={accessControlProvider}>{/* ... */}</Refine>
```

## Vérifier les permissions

Le hook `useCan` interroge le provider depuis vos composants. Il est utile pour masquer un bouton, désactiver une action ou afficher une explication.

```tsx
const { data } = useCan({
  resource: "products",
  action: "delete",
});
```

## Protéger l'interface

`<CanAccess />` permet de protéger une portion de JSX. Les intégrations UI de Refine peuvent aussi utiliser l'access control pour masquer automatiquement certaines actions CRUD.

## Bonnes pratiques

L'UI améliore l'expérience, mais elle ne remplace pas les contrôles côté serveur. Utilisez Refine pour guider l'utilisateur et appliquez les règles critiques dans l'API.
