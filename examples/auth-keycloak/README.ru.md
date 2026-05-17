<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации Keycloak

Этот пример показывает интеграцию **Keycloak** с **Refine**. Keycloak отвечает за realm, client и токены, а приложение использует `authProvider` для проверки доступа к ресурсам Refine.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Что проверить

- Параметры Keycloak realm, client и redirect URI.
- Обновление токена и обработку выхода.
- Поведение защищенных маршрутов при истекшей сессии.
- Сохранение имен API, resources и route paths на английском.

[Открыть пример auth-keycloak в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
