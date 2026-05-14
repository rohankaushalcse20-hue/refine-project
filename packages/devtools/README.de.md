# Refine devtools

`@refinedev/devtools` bietet Entwicklungswerkzeuge fuer Refine-Anwendungen. Es hilft beim Debuggen und Prototyping, etwa durch Monitoring von queries und mutations, Testen von Inferencer-generiertem Code und Verwalten von Refine packages in der UI.

## Verwendung

Installiere zuerst die aktuelle Version von `@refinedev/cli`:

```bash
npm install @refinedev/cli@latest
```

Installiere danach `@refinedev/devtools` ueber die CLI:

```bash
npm run refine devtools init
```

> Falls `@refinedev/cli` noch nicht installiert ist, folge der [installation guide](https://refine.dev/docs/packages/cli/#how-to-add-to-an-existing-project).

Devtools funktionieren nur im Entwicklungsmodus und haben keinen Overhead in production builds.
