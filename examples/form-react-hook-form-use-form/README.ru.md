<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример формы с React Hook Form

Этот пример показывает использование **React Hook Form** вместе с **Refine**. Hook `useForm` связывает отправку данных с CRUD-действиями, а React Hook Form управляет состоянием полей.

## Запуск локально

```bash
npm create refine-app@latest -- --example form-react-hook-form-use-form
```

## Что проверить

- Настройки `useForm` и передачу form props.
- Валидацию, submit и обработку ошибок.
- Сохранение данных через create или edit action.
- То, что hook names, field names и commands не локализованы.

[Открыть пример form-react-hook-form-use-form в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/form-react-hook-form-use-form?view=preview&theme=dark&codemirror=1)
