<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример аутентификации с Mantine

Этот пример демонстрирует, как использовать **Mantine** для страниц входа и защищенного интерфейса Refine. Он показывает, как `authProvider` управляет состоянием пользователя, а Mantine-компоненты отвечают за визуальную часть приложения.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-mantine
```

## Что проверить

- Корректность login, logout и проверки сессии.
- Поведение защищенных ресурсов при отсутствии авторизации.
- Интеграцию Mantine layout и Refine resource routing.
- Неизменность команд, package names и API names.

[Открыть пример auth-mantine в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-mantine?view=preview&theme=dark&codemirror=1)
