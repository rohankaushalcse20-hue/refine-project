---
title: "Concepts généraux | Refine v5"
display_title: "Concepts généraux"
sidebar_label: "Concepts généraux"
description: "Comprenez l'architecture headless, les resources, les providers, les hooks et meta dans Refine."
---

Refine est un framework extensible pour créer rapidement des applications web. Son architecture moderne repose sur des **hooks**, des **providers** connectables et une gestion robuste des données et de l'état.

## Concept headless

Refine n'impose pas un ensemble fermé de composants visuels. Il fournit plutôt des `hooks`, `components`, `providers` et utilitaires qui séparent la logique métier de l'interface.

Cette séparation permet d'utiliser des designs personnalisés ou des frameworks UI comme Tailwind CSS, Ant Design, Material UI, Mantine et Chakra UI tout en gardant les avantages de `@refinedev/core`.

## Resource

Une **resource** représente une entité comme `products`, `blogPosts` ou `orders`. Sa définition relie routes, opérations CRUD, menus et providers dans une structure cohérente.

## Providers

Les providers gèrent les données, l'authentification, l'autorisation, les notifications, l'i18n, le temps réel, le routing et les audit logs. Vous pouvez utiliser ceux fournis par Refine ou créer les vôtres.

## Hooks

Les hooks de Refine sont headless et indépendants de la bibliothèque UI. `useGo`, `useCan` et `useTranslate` donnent une interface unique pour naviguer, vérifier les permissions et traduire.

## Meta

La propriété `meta` transmet des informations supplémentaires aux providers et aux hooks : headers, paramètres spéciaux, sélection de champs, multi-tenancy ou génération de requêtes GraphQL.
