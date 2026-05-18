<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример хука useSelect

Этот пример демонстрирует `useSelect` для загрузки вариантов выбора из data provider. Он подходит для форм Refine, где поля выбора должны получать данные из ресурса, поддерживать поиск и корректно отображать выбранные значения.

## Запуск локально

```bash
npm create refine-app@latest -- --example core-use-select
```

## Что проверить

- Загрузку options через `useSelect`.
- Настройку `optionLabel`, `optionValue` и default value.
- Поведение поиска и обновления списка вариантов.
- Сохранение hook names, field names и API names.

[Открыть пример core-use-select в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-select?view=preview&theme=dark&codemirror=1)
