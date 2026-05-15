# Refine Devtools

`@refinedev/devtools` добавляет инструменты разработки для refine-приложений. Devtools помогают отлаживать запросы и мутации, проверять сгенерированный Inferencer-код, просматривать настройки проекта и быстрее находить проблемы во время разработки.

## Установка

Сначала убедитесь, что установлен актуальный `@refinedev/cli`.

```sh
npm install @refinedev/cli@latest
```

Затем инициализируйте devtools в проекте.

```sh
npm run refine devtools init
```

## Использование

Devtools работают только в development mode и не добавляют накладных расходов в production-сборку. Их можно держать подключенными в проекте без дополнительных действий для исключения из production bundle.

## Документация

- Изучите [документацию Devtools](https://refine.dev/docs/guides-concepts/development/#refine-devtools).
- Если CLI еще не подключен, откройте [инструкцию по установке CLI](https://refine.dev/docs/packages/cli/#how-to-add-to-an-existing-project).
