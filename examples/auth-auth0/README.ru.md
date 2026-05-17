<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации Auth0

Этот пример показывает, как подключить **Auth0** к приложению **Refine** через `authProvider`. Потоки входа, выхода и проверки сессии остаются в Auth0, а ресурсы, маршруты и CRUD-экраны продолжают управляться Refine.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Что проверить

- Настройки Auth0 domain, client ID и redirect URL.
- Обработку login, logout и check в `authProvider`.
- Защиту маршрутов и возврат пользователя после входа.
- Сохранение API names, resources и routes без локализации.

[Открыть пример auth-auth0 в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
