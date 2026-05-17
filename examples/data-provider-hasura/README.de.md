<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Data provider-Beispiel mit Hasura

Dieses Beispiel zeigt, wie **Refine** mit Hasura und GraphQL verbunden wird. Refine resources bleiben die zentrale Struktur der Anwendung, waehrend Hasura die Datenabfragen und Mutationen bereitstellt.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## Wichtige Punkte

- Hasura als GraphQL data provider
- Listen, Erstellen und Bearbeiten ueber Refine resources
- Datenzugriff ueber provider statt direkt in UI-Komponenten
- Befehle, URLs und API-Namen bleiben unveraendert

[Beispiel data-provider-hasura in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
