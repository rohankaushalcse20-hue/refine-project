<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример кастомной страницы входа

Этот пример демонстрирует, как заменить стандартную страницу login в приложении Refine. Он подходит для проектов, где нужен брендированный экран входа, собственные поля формы или особая логика перед вызовом `authProvider.login`.

## Запуск локально

```bash
npm create refine-app@latest -- --example customization-login
```

## Что проверить

- Подключение пользовательского login-компонента.
- Передачу данных формы в `authProvider.login`.
- Обработку ошибок входа и перенаправление после успеха.
- Сохранение route names, commands и API identifiers.

[Открыть пример customization-login в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-login?view=preview&theme=dark&codemirror=1)
