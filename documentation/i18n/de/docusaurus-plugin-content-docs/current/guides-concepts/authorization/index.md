---
title: "Autorisierung | Refine v5"
display_title: "Autorisierung"
sidebar_label: "Autorisierung"
description: "Steuere mit dem Access Control Provider Aktionen, Routen und Komponenten anhand von Berechtigungen."
---

Autorisierung legt fest, was ein angemeldeter User tun darf. In Refine wird sie ueber `accessControlProvider` modelliert und kann in Hooks, Buttons, Menues und Seiten genutzt werden.

## Access Control Provider

Die zentrale Methode ist `can`. Sie erhaelt `resource`, `action` und bei Bedarf weiteren Kontext und gibt dann eine Zugriffsentscheidung zurueck.

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

Mit `useCan` kannst du die UI an Berechtigungen anpassen. Die endgueltige Autorisierungspruefung sollte aber weiterhin im Backend stattfinden.
