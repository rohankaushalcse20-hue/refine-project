<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Data-provider-Beispiel mit Nestjsx CRUD

Dieses Beispiel zeigt, wie **Refine** mit einem Nestjsx CRUD-Backend arbeitet. Der data provider uebersetzt Refine-Operationen in passende Backend-Anfragen und haelt die UI schlank.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example data-provider-nestjsx-crud
```

## Wichtige Punkte

- Nestjsx CRUD als Backend fuer Resources verwenden
- Listen, Details und Mutationen ueber Refine-Hooks ausloesen
- Backend-spezifische Anfrageformate im data provider kapseln
- Commands, URLs und API-Namen unveraendert lassen

[Beispiel data-provider-nestjsx-crud in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-nestjsx-crud?view=preview&theme=dark&codemirror=1)
