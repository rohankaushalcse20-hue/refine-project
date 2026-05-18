<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## MUI-Beispiel fuer `useUpdateMany`

Dieses Beispiel zeigt, wie **Refine** mehrere Datensaetze aus einer MUI-Tabelle aktualisiert. Die Tabelle liefert die Auswahl, Refine fuehrt die Bulk-Mutation aus und haelt den Listenstatus konsistent.

## Lokal ausfuehren

```bash
npm create refine-app@latest -- --example table-mui-use-update-many
```

## Wichtige Punkte

- Mehrere Tabellenzeilen fuer eine gemeinsame Aktion auswaehlen
- `useUpdateMany` fuer Bulk-Aktualisierungen verwenden
- UI-Zustand nach Mutationen aktuell halten
- Befehle, URLs und API-Namen unveraendert lassen

[Beispiel table-mui-use-update-many in CodeSandbox oeffnen](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-mui-use-update-many?view=preview&theme=dark&codemirror=1)
