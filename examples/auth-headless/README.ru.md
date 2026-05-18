<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Headless-пример аутентификации

Этот пример показывает аутентификацию Refine без привязки к конкретной UI-библиотеке. Он подходит для проектов, где интерфейс строится собственными компонентами, а Refine отвечает за ресурсы, маршрутизацию и проверку доступа через `authProvider`.

## Запуск локально

```bash
npm create refine-app@latest -- --example auth-headless
```

## Что проверить

- Реализацию login, logout, check и onError в `authProvider`.
- Как защищенные маршруты реагируют на неавторизованного пользователя.
- Разделение headless-логики Refine и пользовательского UI.
- Сохранение API identifiers и route names в исходном виде.

[Открыть пример auth-headless в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
