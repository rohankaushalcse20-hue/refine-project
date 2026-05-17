<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример data provider для Appwrite

Этот пример показывает подключение **Appwrite** к **Refine** через `dataProvider`. Appwrite хранит данные и выполняет запросы, а Refine предоставляет готовые CRUD-потоки.

## Запуск локально

```bash
npm create refine-app@latest -- --example data-provider-appwrite
```

## Что проверить

- Project ID, endpoint и database settings Appwrite.
- Сопоставление collections с resources Refine.
- Обработку list, show, create и edit операций.
- Сохранение Appwrite SDK names, collection IDs и commands без перевода.

[Открыть пример data-provider-appwrite в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-appwrite?view=preview&theme=dark&codemirror=1)
