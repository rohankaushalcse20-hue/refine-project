<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google Login-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** mit Google Login fuer die Authentifizierung genutzt wird. Der `authProvider` kapselt den externen login flow, waehrend Refine weiterhin resources, routing und geschuetzte Seiten koordiniert.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Wichtige Punkte

- Google Login als externer identity provider
- Geschuetzte Refine-Seiten nach erfolgreicher Anmeldung
- Trennung zwischen Authentifizierung, routing und UI
- Befehle, URLs und API-Namen bleiben unveraendert

[Beispiel auth-google-login in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
