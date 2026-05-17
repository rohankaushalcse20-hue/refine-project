<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** mit Keycloak fuer enterprise authentication verbunden wird. Keycloak uebernimmt die Anmeldung, waehrend Refine resources und Zugriffslogik in der Anwendung strukturiert.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Wichtige Punkte

- Einbindung von Keycloak ueber den `authProvider`
- Geschuetzte routes und authentifizierte resources
- Geeignet fuer Teams mit zentralem identity management
- Befehle, URLs und API-Namen bleiben wie im Original erhalten

[Beispiel auth-keycloak in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
