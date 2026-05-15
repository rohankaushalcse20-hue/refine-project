# Интеграция React Hook Form для refine

`@refinedev/react-hook-form` связывает формы refine с [React Hook Form](https://react-hook-form.com/). Пакет помогает строить формы создания и редактирования с валидацией, состоянием отправки и интеграцией с data provider.

## Установка

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Базовое использование

Используйте `useForm` из `@refinedev/react-hook-form`, чтобы получить свойства формы и связать отправку с ресурсами refine.

```tsx
import { useForm } from "@refinedev/react-hook-form";
```

Интеграция подходит для headless-интерфейсов и кастомных UI-компонентов, где нужно полностью контролировать разметку формы.

## Документация

- Изучите [документацию React Hook Form integration](https://refine.dev/docs/packages/react-hook-form/use-form/).
- Общие принципы форм описаны в [гайде по forms](https://refine.dev/docs/guides-concepts/forms/).
