<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример входа через OTP

Этот пример показывает сценарий аутентификации Refine с одноразовым кодом. Он полезен для проверки пользовательского входа без пароля, где `authProvider` обрабатывает отправку кода, подтверждение и последующий доступ к защищенным ресурсам.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-otp
```

## Что проверить

- Поток запроса и подтверждения одноразового кода.
- Проверку сессии после успешного входа.
- Поведение защищенных страниц при ошибке или истекшем коде.
- Сохранение command names, routes и API identifiers без перевода.

[Открыть пример auth-otp в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
