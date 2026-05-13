---
title: Pendahuluan
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Tutorial ini membawa Anda dari dasar Refine menuju workflow yang lebih lanjut secara bertahap. Saat mengikuti langkah-langkahnya, Anda akan belajar membangun aplikasi CRUD lengkap dengan Refine.

Refine tidak terikat pada satu library routing, sehingga Anda dapat memilih solusi yang paling cocok untuk cara kerja tim. Refine mendukung secara resmi [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js), dan [Remix](/core/docs/routing/integrations/remix). Materi berikutnya akan menyesuaikan pilihan routing Anda, dan pilihan tersebut masih dapat diganti nanti.

Pilih library routing yang ingin Anda ikuti:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

Pada modul berikutnya, Anda juga akan memilih integrasi UI dan mempelajari bagaimana integrasi tersebut dibangun serta kapan cocok digunakan. Refine mendukung Ant Design, Material UI, Mantine, dan Chakra UI secara resmi, tetapi tutorial ini berfokus pada jalur yang paling umum: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) dan [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Pilih framework UI yang ingin Anda ikuti:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Materi untuk library UI lainnya tersedia di [documentation](/core/docs/guides-concepts/ui-libraries).

## Isi tutorial

Berikut bagian tutorial yang dikelompokkan berdasarkan topik:

### Essentials

- [Aplikasi Refine pertama](/core/tutorial/essentials/setup/)
- [Mengambil record](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Memperbarui record](/core/tutorial/essentials/data-fetching/updating-data/)
- [Menampilkan daftar record](/core/tutorial/essentials/data-fetching/listing-data/)
- [Forms](/core/tutorial/essentials/forms/)
- [Tables](/core/tutorial/essentials/tables/)

### Authentication

- [Pendahuluan](/core/tutorial/authentication/intro/)
- [Melindungi konten](/core/tutorial/authentication/protecting-content/)
- [Login dan logout](/core/tutorial/authentication/logging-in-out/)
- [Menggunakan identitas pengguna](/core/tutorial/authentication/user-identity/)
- [Integrasi data provider](/core/tutorial/authentication/data-provider-integration/)

### Routing dengan React Router

- [Pendahuluan](/core/tutorial/routing/intro/react-router/)
- [Authentication](/core/tutorial/routing/authentication/react-router/)
- [Definisi resources](/core/tutorial/routing/resource-definition/react-router/)
- [Navigasi](/core/tutorial/routing/navigation/react-router/)
- [Inferensi parameter](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirects](/core/tutorial/routing/redirects/react-router/)
- [Sinkronisasi state dengan lokasi](/core/tutorial/routing/syncing-state/react-router/)

### Library UI dengan Ant Design

- [Pendahuluan](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Menggunakan layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [Komponen CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Library UI dengan Material UI

- [Pendahuluan](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Menggunakan layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [Komponen CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Langkah berikutnya dengan Ant Design

- [Pendahuluan](/core/tutorial/next-steps/intro/ant-design/)
- [Menggunakan Inferencer](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [Menggunakan CLI](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Menggunakan Devtools](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Ringkasan](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Langkah berikutnya dengan Material UI

- [Pendahuluan](/core/tutorial/next-steps/intro/material-ui/)
- [Menggunakan Inferencer](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [Menggunakan CLI](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Menggunakan Devtools](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Ringkasan](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
