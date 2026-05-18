<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Access-Control-Beispiel mit Cerbos

Dieses Beispiel zeigt, wie **Refine** Cerbos fuer externe Policy-Entscheidungen verwendet. Die Anwendung fragt Berechtigungen zentral ab und kann UI-Aktionen anhand der Antwort anzeigen oder ausblenden.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## Wichtige Punkte

- Cerbos als access control provider anbinden
- Berechtigungen fuer Resources und Aktionen pruefen
- Policy-Logik ausserhalb der UI halten
- Befehle, Provider-Namen und Routen unveraendert verwenden

[Beispiel access-control-cerbos in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
