---
title: Giriş
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Bu tutorial sizi Refine temellerinden daha ileri iş akışlarına adım adım taşır. Adımları izlerken Refine ile tam bir CRUD uygulaması geliştirmeyi öğreneceksiniz.

Refine tek bir routing library'ye bağlı değildir; ekibinizin çalışma biçimine en uygun çözümü seçebilirsiniz. Refine resmi olarak [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) ve [Remix](/core/docs/routing/integrations/remix) destekler. Sonraki içerikler routing seçiminize göre uyarlanır ve bu seçim daha sonra değiştirilebilir.

Takip etmek istediğiniz routing library'yi seçin:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

Sonraki modüllerde UI entegrasyonunu da seçecek, bu entegrasyonların nasıl kurulduğunu ve hangi durumlarda uygun olduğunu öğreneceksiniz. Refine Ant Design, Material UI, Mantine ve Chakra UI için resmi destek sunar; bu tutorial ise en yaygın iki yol olan [Ant Design](/core/docs/ui-integrations/ant-design/introduction) ve [Material UI](/core/docs/ui-integrations/material-ui/introduction) üzerine odaklanır.

Takip etmek istediğiniz UI framework'ü seçin:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Diğer UI library'leri için içerikler [documentation](/core/docs/guides-concepts/ui-libraries) bölümünde bulunabilir.

## Tutorial içeriği

Aşağıdaki bölümler konu başlıklarına göre gruplanmıştır:

### Essentials

- [İlk Refine uygulaması](/core/tutorial/essentials/setup/)
- [Kayıtları alma](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Kayıtları güncelleme](/core/tutorial/essentials/data-fetching/updating-data/)
- [Kayıt listesini gösterme](/core/tutorial/essentials/data-fetching/listing-data/)
- [Forms](/core/tutorial/essentials/forms/)
- [Tables](/core/tutorial/essentials/tables/)

### Authentication

- [Giriş](/core/tutorial/authentication/intro/)
- [İçeriği koruma](/core/tutorial/authentication/protecting-content/)
- [Login ve logout](/core/tutorial/authentication/logging-in-out/)
- [Kullanıcı kimliğini kullanma](/core/tutorial/authentication/user-identity/)
- [Data provider entegrasyonu](/core/tutorial/authentication/data-provider-integration/)

### React Router ile Routing

- [Giriş](/core/tutorial/routing/intro/react-router/)
- [Authentication](/core/tutorial/routing/authentication/react-router/)
- [Resources tanımları](/core/tutorial/routing/resource-definition/react-router/)
- [Navigasyon](/core/tutorial/routing/navigation/react-router/)
- [Parametreleri çıkarma](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirects](/core/tutorial/routing/redirects/react-router/)
- [State'i konumla senkronize etme](/core/tutorial/routing/syncing-state/react-router/)

### Ant Design ile UI library

- [Giriş](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Layouts kullanma](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [CRUD component'leri](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Material UI ile UI library

- [Giriş](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Layouts kullanma](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [CRUD component'leri](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Ant Design ile sonraki adımlar

- [Giriş](/core/tutorial/next-steps/intro/ant-design/)
- [Inferencer kullanma](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [CLI kullanma](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Devtools kullanma](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Özet](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Material UI ile sonraki adımlar

- [Giriş](/core/tutorial/next-steps/intro/material-ui/)
- [Inferencer kullanma](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [CLI kullanma](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Devtools kullanma](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Özet](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
