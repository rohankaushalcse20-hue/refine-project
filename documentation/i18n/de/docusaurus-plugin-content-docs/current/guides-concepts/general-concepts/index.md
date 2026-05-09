---
title: "Grundkonzepte | Refine v5"
display_title: "Grundkonzepte"
sidebar_label: "Grundkonzepte"
description: "Verstehe in Refine die Headless-Architektur, Resources, Provider, Hooks und meta."
---

Refine ist ein erweiterbares Framework, mit dem du Webanwendungen schnell aufbauen kannst. Die Architektur basiert auf **Hooks**, austauschbaren **Providern** und einer verlaesslichen Daten- und Statusverwaltung.

## Headless-Konzept

Refine bindet dich nicht an ein festes UI-Komponenten-Set. Es liefert `hooks`, `components`, `providers` und Utilities, trennt die Geschaeftslogik aber klar von der Darstellung.

Dadurch kannst du mit einem eigenen Design System, Tailwind CSS, Ant Design, Material UI, Mantine oder Chakra UI arbeiten und trotzdem die Vorteile von `@refinedev/core` nutzen.

## Resources

Ein **Resource** beschreibt eine Entitaet in deiner Anwendung, zum Beispiel `products`, `blogPosts` oder `orders`. Resources verknuepfen Routen, CRUD-Aktionen, Menues und Provider in einer klaren Struktur.

## Provider

Provider uebernehmen Aufgaben wie Datenzugriff, Authentifizierung, Autorisierung, Benachrichtigungen, i18n, Realtime, Routing und Audit Logs. Du kannst eingebaute Provider verwenden oder eigene Implementierungen bereitstellen.

## Hooks

Die Hooks von Refine sind headless und nicht an eine UI-Bibliothek gebunden. APIs wie `useGo`, `useCan` oder `useTranslate` geben dir eine einheitliche Schnittstelle fuer Navigation, Berechtigungen und Uebersetzungen.

## Meta

Ueber die Eigenschaft `meta` kannst du zusaetzliche Informationen an Provider und Hooks weitergeben, zum Beispiel Header, spezielle Parameter, Feld-Auswahl, Multi-Tenancy-Kontext oder GraphQL-Abfragen.
