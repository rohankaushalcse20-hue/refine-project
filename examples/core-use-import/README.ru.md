<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример хука useImport

Этот пример показывает, как использовать `useImport` из Refine для загрузки и обработки данных из файла. Он полезен для админ-интерфейсов, где пользователи импортируют записи партиями и ожидают понятной обработки ошибок.

## Запуск локально

```bash
npm create refine-app@latest -- --example core-use-import
```

## Что проверить

- Настройку `useImport` и обработку загруженного файла.
- Как данные отправляются через data provider.
- Поведение при ошибках в строках или сетевых запросах.
- Сохранение hook names, field names и commands без локализации.

[Открыть пример core-use-import в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-import?view=preview&theme=dark&codemirror=1)
