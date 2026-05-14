<div align="center" style="margin: 30px;">
    <a href="https://refine.dev">
    <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
    </a>
</div>

# Refine CLI

`@refinedev/cli` accompagne le développement des applications Refine. Il fournit des commandes pratiques autour du serveur de développement, du build et de la maintenance du projet.

## Installation

```sh
npm install @refinedev/cli
```

## Utilisation

Dans un projet Refine, les scripts peuvent déléguer au runner CLI :

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

Ces commandes conservent le comportement du bundler tout en ajoutant des vérifications utiles, notamment autour des versions de dépendances et des annonces de l'équipe Refine.

## Quand l'utiliser

Utilisez la CLI pour générer un projet avec `create-refine-app`, standardiser les commandes locales et garder une expérience cohérente entre les applications Refine de votre équipe.
