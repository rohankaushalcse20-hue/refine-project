<div align="center" style="margin: 30px;">
    <a href="https://refine.dev">
    <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
    </a>
</div>

# Intégration Material UI pour Refine

`@refinedev/mui` fournit l'intégration Material UI officielle pour construire des applications Refine avec des composants prêts pour la production.

[Material UI](https://mui.com/material-ui/getting-started/) implémente Material Design pour React. Avec Refine, vous pouvez l'utiliser pour livrer rapidement des panels d'administration, dashboards et outils internes tout en gardant la logique métier dans les providers et hooks Refine.

## Installation

```sh
npm install @refinedev/mui @mui/material @mui/lab @mui/x-data-grid @emotion/react @emotion/styled
```

## Démarrage rapide

```sh
npm create refine-app@latest my-refine-app
```

Choisissez Material UI dans l'assistant pour générer un projet avec le thème, le layout et les dépendances nécessaires.

## Ce que fournit le package

- Composants CRUD comme `List`, `Create`, `Edit` et `Show`.
- Hooks spécialisés comme `useDataGrid`, `useAutocomplete`, `useForm` et `useModal`.
- Intégration avec Material UI, notamment `DataGrid`, formulaires, menus, notifications et layouts.
- Base UI cohérente pour les applications Refine headless.

Consultez la [documentation Refine Material UI](https://refine.dev/docs/ui-integrations/material-ui/introduction) pour les guides complets.
