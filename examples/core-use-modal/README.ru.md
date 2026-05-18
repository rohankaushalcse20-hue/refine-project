<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример хука useModal

Этот пример показывает, как `useModal` управляет состоянием модального окна в приложении Refine. Он полезен для сценариев, где создание, редактирование или просмотр данных открываются поверх текущей страницы.

## Запуск локально

```bash
npm create refine-app@latest -- --example core-use-modal
```

## Что проверить

- Открытие и закрытие модального окна через `show` и `close`.
- Передачу состояния в форму или пользовательский компонент.
- Поведение модального сценария при повторном открытии.
- Сохранение hook names, props и commands без перевода.

[Открыть пример core-use-modal в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-modal?view=preview&theme=dark&codemirror=1)
