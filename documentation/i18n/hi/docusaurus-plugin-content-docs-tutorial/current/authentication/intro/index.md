---
title: परिचय
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

अब हमने Refine में data fetching और data manipulation की जरूरी बातें सीख ली हैं। इस unit में हम सीखेंगे कि application में authentication कैसे जोड़ा जाता है और Refine में authentication की मुख्य अवधारणाएं क्या हैं।

Refine एक आसान authentication interface देता है जिसे कम effort में किसी भी authentication provider के साथ उपयोग किया जा सकता है।

इस unit में ये topics cover होंगे:

- Authentication provider बनाकर [`AuthProvider`](/core/docs/authentication/auth-provider) interface सीखना,
- [`useLogin`](/core/docs/authentication/hooks/use-login), [`useIsAuthenticated`](/core/docs/authentication/hooks/use-is-authenticated) hooks और [`<Authenticated />`](/core/docs/authentication/components/authenticated) component जैसे auth hooks और components का उपयोग,
- Data providers में authentication संभालना और authentication errors manage करना।

यह unit router और UI framework agnostic रहेगा। Router और UI framework से जुड़े authentication के हिस्से अगले units में cover किए जाएंगे।

</Sandpack>
