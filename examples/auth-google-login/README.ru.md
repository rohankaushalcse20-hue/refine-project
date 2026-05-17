<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример входа через Google

Этот пример показывает, как использовать Google login в приложении **Refine**. Пользователь проходит аутентификацию через Google, а `authProvider` связывает результат входа с жизненным циклом Refine.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Что проверить

- Конфигурацию Google OAuth client.
- Логику callback, login и logout.
- Защиту CRUD-страниц после проверки сессии.
- То, что команды, переменные окружения и provider names не переведены.

[Открыть пример auth-google-login в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
