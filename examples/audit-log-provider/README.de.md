<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Audit-Log-Provider-Beispiel

Dieses Beispiel zeigt, wie **Refine** Audit-Logs fuer CRUD-Aktionen erfasst. Der audit log provider sammelt Benutzeraktionen, ohne dass Formulare, Tabellen oder Datenzugriffe ihre Grundstruktur aendern muessen.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example audit-log-provider
```

## Wichtige Punkte

- Audit-Log-Ereignisse fuer Resource-Aenderungen erzeugen
- Benutzer, Aktion und Resource nachvollziehbar speichern
- Nachvollziehbarkeit ergaenzen, ohne Datenprovider-Code zu vermischen
- Commands, URLs und Provider-Namen unveraendert verwenden

[Beispiel audit-log-provider in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/audit-log-provider?view=preview&theme=dark&codemirror=1)
