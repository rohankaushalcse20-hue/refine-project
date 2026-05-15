# Inferencer для refine

`@refinedev/inferencer` автоматически генерирует представления для ресурсов на основе структуры данных. Он помогает быстро получить стартовый код для страниц списка, создания, редактирования и просмотра, а затем адаптировать его под продуктовые требования.

## Установка

```sh
npm install @refinedev/inferencer
```

## Базовое использование

Выберите Inferencer-компонент, соответствующий используемой UI-интеграции, и подключите его к ресурсу или маршруту.

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";
```

Inferencer особенно полезен на ранних этапах проекта, когда нужно быстро увидеть рабочий CRUD-интерфейс и получить код, который можно доработать вручную.

## Документация

- Изучите [документацию Inferencer](https://refine.dev/docs/packages/documentation/inferencer/).
- Для базовых принципов ресурсов откройте [документацию Refine component](https://refine.dev/docs/core/refine-component/).
