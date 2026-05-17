<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации Kinde

Этот пример демонстрирует подключение **Kinde** к приложению **Refine**. Kinde управляет identity flow, а `authProvider` передает состояние входа и выхода в интерфейс Refine.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Что проверить

- Конфигурацию Kinde client, domain и callback URL.
- Переходы login и logout из UI.
- Проверку сессии перед отображением protected resources.
- Сохранение терминов Kinde, Refine и API identifiers без перевода.

[Открыть пример auth-kinde в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
