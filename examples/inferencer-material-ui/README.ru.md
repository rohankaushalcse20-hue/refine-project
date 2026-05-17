<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример Inferencer с Material UI

Этот пример показывает, как **Inferencer** в **Refine** может быстро сгенерировать CRUD-экраны на базе **Material UI**. Это удобно для проверки структуры resource перед ручной доработкой страниц.

## Запуск локально

```bash
npm create refine-app@latest -- --example inferencer-material-ui
```

## Что проверить

- Сгенерированные list, show, create и edit pages.
- Соответствие полей данным, которые возвращает `dataProvider`.
- Компоненты Material UI, выбранные Inferencer.
- Сохранение component names, resource names и command syntax без перевода.

[Открыть пример inferencer-material-ui в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/inferencer-material-ui?view=preview&theme=dark&codemirror=1)
