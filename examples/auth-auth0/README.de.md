<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** mit einem Auth0 login flow verbunden wird. Die Anwendung behaelt resources und providers von Refine bei, waehrend Auth0 die Benutzeridentitaet verwaltet.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Wichtige Punkte

- Integration von `authProvider` mit Auth0
- Geschuetzte Routen und authentifizierte resources
- Externer login flow ohne Aenderung der Refine-Struktur
- Befehle, URLs und API-Namen bleiben wie im Originalbeispiel erhalten

[Beispiel auth-auth0 in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
