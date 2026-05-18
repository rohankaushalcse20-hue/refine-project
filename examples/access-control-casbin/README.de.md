<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Access-Control-Beispiel mit Casbin

Dieses Beispiel zeigt, wie **Refine** Casbin fuer rollen- und regelbasierte Berechtigungen nutzt. Die Zugriffskontrolle bleibt im access control provider, waehrend Resources, Routen und UI-Komponenten unveraendert bleiben.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## Wichtige Punkte

- Casbin-Regeln in Refine einbinden
- Aktionen wie `list`, `create`, `edit` und `delete` pruefen
- Sichtbarkeit von Buttons und Seiten ueber Berechtigungen steuern
- Bestehende Resource-Namen und API-Aufrufe unveraendert lassen

[Beispiel access-control-casbin in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
