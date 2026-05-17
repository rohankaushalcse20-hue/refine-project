<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример data provider для Strapi

Этот пример показывает, как подключить **Strapi** API к приложению **Refine**. Refine использует `dataProvider` для CRUD-операций, а Strapi остается источником контента и схем.

## Запуск локально

```bash
npm create refine-app@latest -- --example data-provider-strapi
```

## Что проверить

- Base URL и параметры API Strapi.
- Чтение, создание и обновление записей через resources.
- Обработку pagination, filters и сортировки.
- Сохранение route names, endpoint paths и команд без локализации.

[Открыть пример data-provider-strapi в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi?view=preview&theme=dark&codemirror=1)
