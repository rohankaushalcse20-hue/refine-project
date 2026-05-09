---
title: "UI-Bibliotheken | Refine v5"
display_title: "UI-Bibliotheken"
sidebar_label: "UI-Bibliotheken"
description: "Verstehe, wie die UI-Integrationen von Refine funktionieren und wann sich ihre Komponenten, Hooks und Provider lohnen."
---

Die UI-Integrationen von Refine erweitern die Kernfunktionen um Hooks und Komponenten, die mit wenig zusaetzlicher Bibliothekslogik einsatzbereit sind. Du kannst die passende UI-Bibliothek waehlen, ohne die Anwendungslogik daran zu koppeln.

Die Headless-Architektur erlaubt es dir ausserdem, eigene Komponenten oder komplett eigene Integrationen zu bauen. Logik bleibt in Hooks, Helpern und logischen Komponenten gekapselt.

## Verfuegbare Integrationen

Refine bietet direkte Integrationen fuer vier haeufig genutzte Bibliotheken im React-Oekosystem:

- [Ant Design mit `@refinedev/antd`](/core/docs/ui-integrations/ant-design/introduction/)
- [Material UI mit `@refinedev/mui`](/core/docs/ui-integrations/material-ui/introduction/)
- [Chakra UI mit `@refinedev/chakra-ui`](/core/docs/ui-integrations/chakra-ui/introduction/)
- [Mantine mit `@refinedev/mantine`](/core/docs/ui-integrations/mantine/introduction/)

## Vorgefertigte Bausteine

Die UI-Pakete bringen Layouts, Menues, Buttons, Views, Feld-Komponenten und Auth-Seiten mit. Diese Bausteine kombinieren die Logik von Refine mit dem Designsystem der jeweiligen Bibliothek.

## Anpassung

Du kannst Komponenten ueber Props anpassen, globale Optionen im `<Refine>`-Setup definieren oder ueber `swizzle` einzelne UI-Komponenten exportieren und selbst pflegen.

## Benachrichtigungen

Auch die Notification-Systeme der UI-Bibliotheken koennen ueber `notificationProvider` an Refine angebunden werden, damit CRUD-Aktionen und Fehler konsistent rueckgemeldet werden.
