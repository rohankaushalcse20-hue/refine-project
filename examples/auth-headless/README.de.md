<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Headless-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** Authentifizierung ohne festes UI-Framework abbildet. Der auth provider kapselt die Sitzungslogik, waehrend die Darstellung vollstaendig in der Anwendung bleibt.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-headless
```

## Wichtige Punkte

- Login, Logout und Identity ueber den auth provider steuern
- Eigene Komponenten fuer Auth-Seiten verwenden
- Geschuetzte Seiten ueber Refine-Routing absichern
- API-Namen, Hooks und Commands unveraendert uebernehmen

[Beispiel auth-headless in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
