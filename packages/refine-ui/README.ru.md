# Refine UI registry

`@refinedev/refine-ui` содержит registry-шаблон для компонентов, hooks, pages и других файлов, совместимых с `shadcn` CLI. Его можно использовать как основу для собственного component registry на Next.js.

## Использование

- `registry.json` описывает элементы registry и связанные файлы.
- Команда `shadcn build` собирает registry.
- Скомпилированные элементы отдаются как статические JSON-файлы из `public/r/[name].json`.
- Элементы registry совместимы с `shadcn` CLI.

## Документация

Полный формат registry описан в [документации shadcn](https://ui.shadcn.com/docs/registry).
