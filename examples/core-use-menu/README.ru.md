<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример хука useMenu

Этот пример демонстрирует `useMenu`, который строит меню на основе resources Refine. Он помогает проверить структуру навигации, вложенные элементы и связь пунктов меню с маршрутами приложения.

## Запуск локально

```bash
npm create refine-app@latest -- --example core-use-menu
```

## Что проверить

- Формирование пунктов меню из resource definitions.
- Поддержку вложенных пунктов и активного состояния.
- Связь `useMenu` с router provider.
- Неизменность resource names, route paths и hook names.

[Открыть пример core-use-menu в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-menu?view=preview&theme=dark&codemirror=1)
