<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## OTP-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** einen Login mit Einmalpasswort abbildet. Der auth provider koordiniert die OTP-Pruefung und stellt danach die ueblichen Auth-Funktionen fuer die Anwendung bereit.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-otp
```

## Wichtige Punkte

- OTP-Anforderung und Verifizierung im Auth-Flow abbilden
- Erfolgreiche Anmeldung an Refine weitergeben
- Geschuetzte Resources erst nach gueltiger Sitzung anzeigen
- Befehle, Provider-Methoden und API-Namen unveraendert verwenden

[Beispiel auth-otp in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
