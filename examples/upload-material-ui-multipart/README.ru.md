<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример multipart upload с Material UI

Этот пример показывает загрузку файлов в приложении **Refine** с интерфейсом **Material UI**. Форма отправляет multipart data, а CRUD-поток остается связанным с resource action.

## Запуск локально

```bash
npm create refine-app@latest -- --example upload-material-ui-multipart
```

## Что проверить

- Выбор файла и формирование multipart request.
- Интеграцию upload field с формой Material UI.
- Обработку success, error и loading state.
- Сохранение endpoint paths, field names и commands без перевода.

[Открыть пример upload-material-ui-multipart в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/upload-material-ui-multipart?view=preview&theme=dark&codemirror=1)
