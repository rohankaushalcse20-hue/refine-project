<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример data provider для Airtable

Этот пример показывает, как **Refine** работает с **Airtable** через `dataProvider`. CRUD-операции Refine сопоставляются с таблицами Airtable, а приложение остается построенным вокруг resources.

## Запуск локально

```bash
npm create refine-app@latest -- --example data-provider-airtable
```

## Что проверить

- Настройки Airtable base ID, table name и API token.
- Вызовы list, create, edit и delete через `dataProvider`.
- Отображение записей Airtable в CRUD-страницах.
- Сохранение команд, endpoint names и resource identifiers без перевода.

[Открыть пример data-provider-airtable в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-airtable?view=preview&theme=dark&codemirror=1)
