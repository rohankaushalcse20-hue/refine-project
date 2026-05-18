<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации с Ant Design

Этот пример показывает, как собрать экран входа и защищенные CRUD-страницы Refine с компонентами **Ant Design**. Он полезен, если нужно проверить связку `authProvider`, роутов, ресурсов и готового UI без ручной сборки всего приложения.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-antd
```

## Что проверить

- Поведение входа, выхода и проверки сессии через `authProvider`.
- Отображение защищенных страниц после успешной аутентификации.
- Совместимость Ant Design-компонентов с layout Refine.
- Сохранение имен ресурсов, API names и routes без локализации.

[Открыть пример auth-antd в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-antd?view=preview&theme=dark&codemirror=1)
