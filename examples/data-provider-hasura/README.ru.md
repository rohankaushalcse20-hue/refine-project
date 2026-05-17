<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример data provider для Hasura

Этот пример показывает, как использовать **Hasura** GraphQL backend с **Refine**. `dataProvider` отправляет GraphQL-запросы, а Refine сохраняет привычную модель resources и actions.

## Запуск локально

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## Что проверить

- GraphQL endpoint и admin secret Hasura.
- Генерацию запросов для list, show, create и update.
- Связь таблиц Hasura с resources Refine.
- Сохранение GraphQL field names, operation names и commands без перевода.

[Открыть пример data-provider-hasura в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
