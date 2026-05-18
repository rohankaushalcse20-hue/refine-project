<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример command palette с kbar

Этот пример показывает, как добавить в приложение Refine командную палитру на базе **kbar**. Палитра помогает быстро переходить между ресурсами, выполнять действия и улучшать навигацию в админ-панелях с большим числом страниц.

## Запуск локально

```bash
npm create refine-app@latest -- --example command-palette-kbar
```

## Что проверить

- Регистрацию команд для resources и пользовательских действий.
- Открытие палитры и переходы по выбранным пунктам.
- Совместимость kbar с routing и layout Refine.
- Неизменность package names, hotkey identifiers и commands.

[Открыть пример command-palette-kbar в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/command-palette-kbar?view=preview&theme=dark&codemirror=1)
