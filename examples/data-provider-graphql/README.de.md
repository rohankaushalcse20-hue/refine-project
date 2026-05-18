<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Data-provider-Beispiel mit GraphQL

Dieses Beispiel zeigt, wie **Refine** ueber einen GraphQL data provider mit einem Backend arbeitet. Queries und Mutations werden hinter der Refine-Resource-Schicht gekapselt.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example data-provider-graphql
```

## Wichtige Punkte

- GraphQL als Datenquelle fuer Refine konfigurieren
- CRUD-Aktionen in Queries und Mutations uebersetzen
- UI-Seiten von Backend-Details entkoppeln
- Commands, URLs und API-Namen unveraendert verwenden

[Beispiel data-provider-graphql in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/master/examples/data-provider-graphql?view=preview&theme=dark&codemirror=1)
