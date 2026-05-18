<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Базовый headless-пример

Этот пример показывает минимальную настройку Refine без готовой UI-интеграции. Он полезен, когда нужно взять resource management, routing и data hooks Refine, но полностью контролировать разметку и компоненты приложения.

## Запуск локально

```bash
npm create refine-app@latest -- --example base-headless
```

## Что проверить

- Подключение `Refine` и объявление resources.
- Использование data hooks без UI-оберток конкретной библиотеки.
- Как проект разделяет бизнес-логику и пользовательскую разметку.
- Сохранение hook names, API identifiers и commands без перевода.

[Открыть пример base-headless в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-headless?view=preview&theme=dark&codemirror=1)
