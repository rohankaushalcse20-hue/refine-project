<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Пример live provider с Ably

Этот пример показывает, как использовать **Ably** для live updates в **Refine**. `liveProvider` получает события в реальном времени, а списки и записи обновляются без ручной перезагрузки.

## Запуск локально

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## Что проверить

- Ably API key и channel configuration.
- Подписку resources на live events.
- Обновление list и show views при изменениях.
- Сохранение event names, provider API и команд без перевода.

[Открыть пример live-provider-ably в CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
