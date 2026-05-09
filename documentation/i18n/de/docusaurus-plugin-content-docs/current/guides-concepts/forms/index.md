---
title: "Formulare | Refine v5"
display_title: "Formulare"
sidebar_label: "Formulare"
description: "Baue CRUD-Formulare mit Refine, UI-Integrationen und Server-Validierung."
---

Formulare sind ein zentraler Teil fast jeder nutzerorientierten Anwendung. Refine stellt Hooks und Komponenten bereit, die Felder, Data Provider, Validierung und Mutationen sinnvoll verbinden.

## Typischer Ansatz

Du kannst Ant Design, Material UI, Mantine, Chakra UI oder React Hook Form einsetzen. Die Logik von Refine bleibt von der UI getrennt, sodass du die Bibliothek passend zum Produkt auswaehlen kannst.

## Create und Edit

`useForm`, `useModalForm`, `useDrawerForm` und `useStepsForm` helfen dir dabei, Create-, Edit- und mehrstufige Flows umzusetzen.

```tsx
const { formProps, saveButtonProps } = useForm({
  resource: "products",
  action: "edit",
});
```

## Beziehungen und Validierung

Mit `useSelect` laedst du Optionen aus verwandten Resources. Fuer mehrsprachige Anwendungen solltest du lokale Validierung, Server-Fehler und i18n-basierte Meldungen zusammen einsetzen.
