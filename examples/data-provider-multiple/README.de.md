<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Beispiel mit mehreren data providern

Dieses Beispiel zeigt, wie **Refine** mehrere data provider in einer Anwendung verwendet. Resources koennen gezielt einem Backend zugeordnet werden, ohne die Seitenlogik zu duplizieren.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example data-provider-multiple
```

## Wichtige Punkte

- Mehrere data provider registrieren
- Resources einem bestimmten Provider zuweisen
- Getrennte Backends in einer Refine-App nutzen
- Provider-Namen, Commands und Routen unveraendert lassen

[Beispiel data-provider-multiple in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-multiple?view=preview&theme=dark&codemirror=1)
