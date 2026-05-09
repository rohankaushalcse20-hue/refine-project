---
title: "Deployment | Refine v5"
display_title: "Deployment"
sidebar_label: "Deployment"
description: "Stelle Refine-Anwendungen auf Basis von Vite, Next.js oder Remix mit sicheren und reproduzierbaren Prozessen bereit."
---

Als Meta-Framework erzwingt Refine keine eigene Deployment-Konfiguration.

Refine-Anwendungen basieren in der Regel auf einem der folgenden Frameworks. Deshalb kannst du dich beim Deployment an deren offiziellen Leitfaeden orientieren:

- [Deployment-Leitfaden fuer Vite](https://vitejs.dev/guide/static-deploy.html)
- [Deployment-Leitfaden fuer Next.js](https://nextjs.org/docs/deployment)
- [Deployment-Leitfaden fuer Remix](https://remix.run/docs/en/main/guides/deployment)

Zur Vereinfachung pflegt das Team das GitHub-Repository [refinedev/Dockerfiles](https://github.com/refinedev/dockerfiles). Dort findest du Dockerfiles fuer die genannten Frameworks.

Diese Dockerfiles orientieren sich an den offiziellen Beispielen der jeweiligen Frameworks und nutzen [refinedev/node](https://hub.docker.com/r/refinedev/node) als Basis-Image mit dem `non-root`-User `refine:nodejs`.

In der finalen Stage laeuft die Anwendung unter `refine:nodejs`, was die **Sicherheit** verbessert und nur die benoetigten Produktionsabhaengigkeiten enthaelt.
