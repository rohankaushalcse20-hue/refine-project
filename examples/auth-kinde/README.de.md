<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde-Authentifizierungsbeispiel

Dieses Beispiel zeigt, wie **Refine** mit Kinde als Authentifizierungsanbieter genutzt wird. Die Integration haelt den login flow ausserhalb der CRUD-Logik und laesst Refine die resources der Anwendung verwalten.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Wichtige Punkte

- Kinde-Integration ueber den `authProvider`
- Anmeldung, Abmeldung und geschuetzte Inhalte
- Klare Trennung zwischen identity provider und Refine resources
- Befehle, URLs und API-Namen bleiben unveraendert

[Beispiel auth-kinde in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
