<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации с Chakra UI

Этот пример демонстрирует, как подключить аутентификацию в приложении Refine с интерфейсом на **Chakra UI**. Он помогает проверить, как `authProvider` управляет входом, выходом и доступом к ресурсам, пока визуальные элементы остаются в стиле Chakra UI.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-chakra-ui
```

## Что проверить

- Потоки login, logout и check в `authProvider`.
- Защиту маршрутов и возврат пользователя после входа.
- Согласованность Chakra UI-компонентов с layout Refine.
- Неизменность package names, команд и routes.

[Открыть пример auth-chakra-ui в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-chakra-ui?view=preview&theme=dark&codemirror=1)
