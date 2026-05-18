<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример OffLayoutArea

Этот пример показывает, как использовать область `OffLayoutArea` рядом с основным layout Refine. Такой подход удобен для глобальных виджетов, уведомлений, плавающих действий или панелей, которые не должны быть частью контента ресурса.

## Запуск локально

```bash
npm create refine-app@latest -- --example customization-offlayout-area
```

## Что проверить

- Где подключается `OffLayoutArea` в layout-компоненте.
- Отображение глобального UI независимо от текущего ресурса.
- Совместимость с навигацией и защищенными страницами.
- Неизменность component names, imports и commands.

[Открыть пример customization-offlayout-area в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-offlayout-area?view=preview&theme=dark&codemirror=1)
