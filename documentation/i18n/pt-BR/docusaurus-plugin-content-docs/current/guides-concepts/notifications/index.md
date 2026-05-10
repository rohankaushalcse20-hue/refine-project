---
title: "Notificações | Refine v5"
display_title: "Notificações"
sidebar_label: "Notificações"
description: "Mostre mensagens de sucesso e erro com o notification provider do Refine."
---

Notificações ajudam a pessoa usuária a entender imediatamente o resultado de uma ação ou um erro ocorrido. O Refine exibe essas mensagens por meio de `notificationProvider` em hooks, mutações e componentes.

## Notification Provider

Um provider normalmente implementa `open` e, com frequência, também `close`.

```tsx
const notificationProvider = {
  open: ({ type, message, description }) => {
    console.log(type, message, description);
  },
  close: (key) => console.log("close", key),
};
```

Integrações com Ant Design, Material UI, Mantine ou Chakra UI podem conectar diretamente seus próprios sistemas de notificação ao Refine.

Em uma aplicação localizada, títulos e descrições também devem ser traduzidos para que o feedback fique claro para o público-alvo.
