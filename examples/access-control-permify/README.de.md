<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Access-Control-Beispiel mit Permify

Dieses Beispiel zeigt, wie **Refine** Permify fuer beziehungsbasierte Zugriffskontrolle nutzt. Berechtigungen werden ueber einen access control provider abgefragt, damit die UI nur erlaubte Aktionen anbietet.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example access-control-permify
```

## Wichtige Punkte

- Permify als Berechtigungsdienst einbinden
- Resource-Aktionen mit `can` pruefen
- Rollen, Beziehungen und Aktionen getrennt von Komponenten modellieren
- Bestehende Refine-Resources und API-Namen unveraendert lassen

[Beispiel access-control-permify in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
