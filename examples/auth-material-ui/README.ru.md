<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации с Material UI

Этот пример показывает, как собрать страницы входа и защищенный CRUD-интерфейс **Refine** с компонентами **Material UI**. `authProvider` управляет доступом, а Material UI отвечает за визуальный слой.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## Что проверить

- Форму входа и обработку ошибок аутентификации.
- Перенаправление пользователя на защищенные страницы.
- Компоненты Material UI, используемые в layout.
- То, что prop names, hooks и route paths сохранены без локализации.

[Открыть пример auth-material-ui в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
