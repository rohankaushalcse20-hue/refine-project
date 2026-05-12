---
title: "Deployment गाइड | Refine v5"
display_title: "Deployment"
sidebar_label: "Deployment"
description: "Refine apps को deploy करते समय framework-specific guides, Dockerfiles और production image considerations का Hindi परिचय।"
---

Refine एक meta-framework है, इसलिए इसकी अपनी कोई fixed deployment configuration नहीं होती।

अधिकांश Refine applications नीचे दिए गए frameworks के ऊपर बनाई जाती हैं। इसलिए deployment के लिए आम तौर पर उन्हीं frameworks की official guides का पालन किया जाता है।

- [Vite deployment guide](https://vitejs.dev/guide/static-deploy.html)
- [Next.js deployment guide](https://nextjs.org/docs/deployment)
- [Remix deployment guide](https://remix.run/docs/en/main/guides/deployment)

सुविधा के लिए हमने [refinedev/Dockerfiles](https://github.com/refinedev/dockerfiles) GitHub repository बनाई है, जिसमें ऊपर बताए गए frameworks के लिए तैयार Dockerfiles मिलते हैं।

ये Dockerfiles संबंधित official Dockerfile examples पर आधारित हैं और base image के रूप में [refinedev/node](https://hub.docker.com/r/refinedev/node) का उपयोग करते हैं, जिसमें `non-root` `refine:nodejs` user उपलब्ध रहता है।

अंतिम stage application को `non-root` `refine:nodejs` user के रूप में चलाती है। इससे **security** बेहतर रहती है और image में केवल production के लिए जरूरी dependencies ही शामिल रहती हैं, जिससे size छोटा रहता है।
