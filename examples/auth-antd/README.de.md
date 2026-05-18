<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Authentifizierungsbeispiel mit Ant Design

Dieses Beispiel zeigt, wie **Refine** Authentifizierung mit Ant Design-Oberflaechen kombiniert. Der auth provider uebernimmt Login, Logout und Sitzungspruefung, waehrend Ant Design die Seiten und Formulare darstellt.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example auth-antd
```

## Wichtige Punkte

- Login- und Logout-Flows mit dem auth provider verbinden
- Geschuetzte Ressourcen erst nach erfolgreicher Anmeldung anzeigen
- Ant Design-Komponenten fuer Auth-Seiten verwenden
- Refine-Provider, Routen und API-Namen unveraendert lassen

[Beispiel auth-antd in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-antd?view=preview&theme=dark&codemirror=1)
