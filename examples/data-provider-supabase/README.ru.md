<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример data provider для Supabase

Этот пример показывает, как **Refine** работает с **Supabase**. Supabase предоставляет database и API, а `dataProvider` связывает их с CRUD-действиями Refine.

## Запуск локально

```bash
npm create refine-app@latest -- --example data-provider-supabase
```

## Что проверить

- Supabase URL и anon key.
- Сопоставление таблиц Supabase с resources.
- Работу list, create, edit и delete в интерфейсе.
- Сохранение Supabase client options, commands и API names без перевода.

[Открыть пример data-provider-supabase в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-supabase?view=preview&theme=dark&codemirror=1)
