<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример таблицы Ant Design

Этот пример показывает, как использовать **Ant Design Table** с **Refine**. Hook `useTable` подключает pagination, filters и sorting к `dataProvider`, а Ant Design отображает таблицу.

## Запуск локально

```bash
npm create refine-app@latest -- --example table-antd-use-table
```

## Что проверить

- Передачу table props из `useTable` в Ant Design.
- Пагинацию, сортировку и фильтры.
- Переходы к show, edit и create actions.
- Сохранение component names, hook names и command syntax без перевода.

[Открыть пример table-antd-use-table в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/table-antd-use-table?view=preview&theme=dark&codemirror=1)
