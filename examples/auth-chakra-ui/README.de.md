<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Authentifizierungsbeispiel mit Chakra UI

Dieses Beispiel zeigt, wie **Refine** einen auth provider mit Chakra UI verbindet. Authentifizierungslogik und visuelle Komponenten bleiben getrennt, damit die Anmeldung leicht angepasst werden kann.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-chakra-ui
```

## Wichtige Punkte

- Auth-Status ueber den Refine auth provider pruefen
- Chakra UI fuer Login-Ansicht und Layout verwenden
- Geschuetzte Bereiche anhand der Sitzung steuern
- Commands, Resource-Namen und Provider-APIs unveraendert lassen

[Beispiel auth-chakra-ui in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-chakra-ui?view=preview&theme=dark&codemirror=1)
