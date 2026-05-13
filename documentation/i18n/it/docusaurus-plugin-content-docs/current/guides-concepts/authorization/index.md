---
title: "Authorization | Refine v5"
display_title: "Authorization"
sidebar_label: "Authorization"
description: "Applica controlli di accesso per resource e action in Refine con access control provider."
---

Authorization determina quali azioni può compiere un utente autenticato. Refine centralizza questo comportamento tramite `accessControlProvider`.

## Access control provider

`accessControlProvider.can` restituisce lo stato di permesso per una specifica coppia `resource` e `action`. Il risultato può guidare accesso alle pagine, visibilità dei button o comportamento dei form.

```ts title=accessControlProvider.ts
export const accessControlProvider = {
  can: async ({ resource, action, params }) => {
    if (resource === "posts" && action === "delete") {
      return { can: false, reason: "Non hai il permesso di eliminare." };
    }

    return { can: true };
  },
};
```

## Uso nella UI

`useCan` e i componenti delle integrazioni UI con supporto access control mostrano l'interfaccia corretta in base al risultato del controllo. Le regole di permesso diventano visibili anche nell'esperienza utente, non solo nel backend.

## Modello resource e action

Le regole sono spesso espresse con action come `list`, `show`, `create`, `edit` e `delete`. Il campo `params` può trasportare contesto aggiuntivo, come record id, tenant o role.

## Controllo backend

L'access control frontend migliora l'esperienza utente, ma non sostituisce i controlli di sicurezza del backend. L'API deve sempre applicare le proprie regole di authorization.
