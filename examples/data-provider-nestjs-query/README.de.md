<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Data-provider-Beispiel mit NestJS Query

Dieses Beispiel zeigt, wie **Refine** den NestJS Query data provider nutzt. Die Anwendung kann Listen, Details und Mutationen ueber Refine-Resources steuern, waehrend die Backend-Integration im Provider bleibt.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example data-provider-nestjs-query
```

## Wichtige Punkte

- NestJS Query als data provider konfigurieren
- Filter, Sortierung und Pagination ueber Refine uebergeben
- CRUD-Seiten von Backend-spezifischem Code entkoppeln
- Commands, Provider-Namen und API-Begriffe unveraendert lassen

[Beispiel data-provider-nestjs-query in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-nestjs-query?view=preview&theme=dark&codemirror=1)
