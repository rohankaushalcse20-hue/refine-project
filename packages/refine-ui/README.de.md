# registry-template

Du kannst die `shadcn` CLI verwenden, um eine eigene Komponenten-Registry zu betreiben. Eine eigene Registry ermoeglicht es, benutzerdefinierte components, hooks, pages und andere Dateien an jedes React-Projekt zu verteilen.

> [!IMPORTANT]
> Diese Vorlage verwendet Tailwind v4. Fuer Tailwind v3 siehe [registry-template](https://github.com/shadcn-ui/registry-template).

## Erste Schritte

Dies ist eine Vorlage zum Erstellen einer benutzerdefinierten Registry mit Next.js.

- Die Vorlage verwendet eine `registry.json` Datei, um components und ihre Dateien zu definieren.
- Der Befehl `shadcn build` wird zum Erstellen der Registry verwendet.
- Registry-items werden als statische Dateien unter `public/r/[name].json` bereitgestellt.
- Die Vorlage enthaelt auch einen route handler zum Ausliefern von Registry-items.
- Jedes Registry-item ist mit der `shadcn` CLI kompatibel.
- Ausserdem ist eine v0-Integration ueber die `Open in v0` API enthalten.

## Dokumentation

Besuche die [shadcn Dokumentation](https://ui.shadcn.com/docs/registry), um die vollstaendige Dokumentation zu lesen.
