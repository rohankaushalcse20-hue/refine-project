<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Authentifizierungsbeispiel mit Mantine

Dieses Beispiel zeigt, wie **Refine** Authentifizierung mit Mantine-Komponenten kombiniert. Die Provider-Struktur bleibt gleich, waehrend Layout, Formulare und Statusmeldungen aus Mantine kommen.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-mantine
```

## Wichtige Punkte

- Mantine-Formulare fuer Login und Auth-Seiten nutzen
- Sitzungsstatus ueber den Refine auth provider lesen
- Navigations- und Resource-Zugriff nach Anmeldung steuern
- Code-APIs, Routen und Commands unveraendert lassen

[Beispiel auth-mantine in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-mantine?view=preview&theme=dark&codemirror=1)
