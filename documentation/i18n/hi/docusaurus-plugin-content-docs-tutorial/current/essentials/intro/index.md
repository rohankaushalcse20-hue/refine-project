---
title: परिचय
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

यह ट्यूटोरियल आपको Refine की बुनियादी अवधारणाओं से लेकर आगे के workflow तक क्रमवार ले जाता है। इसे पूरा करते हुए आप Refine के साथ एक पूरी CRUD application बनाना सीखेंगे।

Refine router-agnostic है, इसलिए आप अपनी सुविधा के अनुसार routing library चुन सकते हैं। Refine [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) और [Remix](/core/docs/routing/integrations/remix) के लिए आधिकारिक support देता है। आगे के चरणों में चुने गए routing विकल्प के अनुसार content बदलेगा। आप किसी भी समय विकल्प बदलकर दूसरी libraries के लिए समान सामग्री भी देख सकते हैं।

जिस routing library के साथ आगे बढ़ना है, उसे चुनें:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

अगले units में आप Refine की UI integrations भी चुनेंगे और देखेंगे कि वे कैसे बनाई जाती हैं और किन स्थितियों में उपयोगी होती हैं। Refine Ant Design, Material UI, Mantine और Chakra UI को officially support करता है, लेकिन यह ट्यूटोरियल खास तौर पर अधिक प्रचलित [Ant Design](/core/docs/ui-integrations/ant-design/introduction) और [Material UI](/core/docs/ui-integrations/material-ui/introduction) flows पर केंद्रित है।

जिस UI framework के साथ आगे बढ़ना है, उसे चुनें:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

अन्य UI libraries के लिए समकक्ष सामग्री आप [documentation](/core/docs/guides-concepts/ui-libraries) में देख सकते हैं।

## ट्यूटोरियल की सामग्री

नीचे ट्यूटोरियल के सभी sections विषय के अनुसार व्यवस्थित किए गए हैं:

### मूल बातें

- [पहला Refine app](/core/tutorial/essentials/setup/)
- [एक record प्राप्त करना](/core/tutorial/essentials/data-fetching/fetching-data/)
- [एक record अपडेट करना](/core/tutorial/essentials/data-fetching/updating-data/)
- [records की सूची दिखाना](/core/tutorial/essentials/data-fetching/listing-data/)
- [Forms](/core/tutorial/essentials/forms/)
- [Tables](/core/tutorial/essentials/tables/)

### Authentication

- [परिचय](/core/tutorial/authentication/intro/)
- [कंटेंट को सुरक्षित करना](/core/tutorial/authentication/protecting-content/)
- [लॉग इन और लॉग आउट](/core/tutorial/authentication/logging-in-out/)
- [user identity का उपयोग](/core/tutorial/authentication/user-identity/)
- [data provider integration](/core/tutorial/authentication/data-provider-integration/)

### React Router के साथ Routing

- [परिचय](/core/tutorial/routing/intro/react-router/)
- [Authentication](/core/tutorial/routing/authentication/react-router/)
- [resources परिभाषित करना](/core/tutorial/routing/resource-definition/react-router/)
- [Navigation](/core/tutorial/routing/navigation/react-router/)
- [parameters infer करना](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirects](/core/tutorial/routing/redirects/react-router/)
- [state को location के साथ sync करना](/core/tutorial/routing/syncing-state/react-router/)

### Ant Design के साथ UI Libraries

- [परिचय](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [layouts का उपयोग](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [CRUD components](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Material UI के साथ UI Libraries

- [परिचय](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [layouts का उपयोग](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactoring](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [CRUD components](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notifications](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Authentication](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Ant Design के साथ अगले कदम

- [परिचय](/core/tutorial/next-steps/intro/ant-design/)
- [Inferencer का उपयोग](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [CLI का उपयोग](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Devtools का उपयोग](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [सारांश](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Material UI के साथ अगले कदम

- [परिचय](/core/tutorial/next-steps/intro/material-ui/)
- [Inferencer का उपयोग](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [CLI का उपयोग](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Devtools का उपयोग](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [सारांश](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
