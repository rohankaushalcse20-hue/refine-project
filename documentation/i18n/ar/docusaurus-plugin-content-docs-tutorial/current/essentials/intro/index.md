---
title: مقدمة
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

يأخذك هذا الدرس من أساسيات Refine إلى خطوات العمل المتقدمة بصورة تدريجية. ومع متابعة الخطوات ستتعلّم كيف تبني تطبيق CRUD كاملاً باستخدام Refine.

Refine لا يرتبط بمكتبة توجيه واحدة، لذلك يمكنك اختيار الحل الأقرب إلى أسلوب فريقك. يدعم Refine رسمياً [React Router DOM](/core/docs/routing/integrations/react-router) و[Next.js](/core/docs/routing/integrations/next-js) و[Remix](/core/docs/routing/integrations/remix). وستتغير المواد اللاحقة بحسب خيار التوجيه الذي تحدده، مع إمكانية تبديله لاحقاً.

اختر مكتبة التوجيه التي تريد المتابعة بها:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

في الوحدات التالية ستختار أيضاً تكامل واجهة المستخدم وتتعرف على كيفية بناء هذه التكاملات ومتى تكون مناسبة. يدعم Refine رسمياً Ant Design وMaterial UI وMantine وChakra UI، لكن هذا الـ tutorial يركّز على أكثر المسارات شيوعاً: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) و[Material UI](/core/docs/ui-integrations/material-ui/introduction).

اختر إطار واجهة المستخدم الذي تريد المتابعة به:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

يمكنك العثور على المواد المقابلة لبقية مكتبات الواجهة ضمن [documentation](/core/docs/guides-concepts/ui-libraries).

## محتويات الدرس

فيما يلي أقسام الـ tutorial مرتبة حسب الموضوع:

### الأساسيات

- [أول تطبيق Refine](/core/tutorial/essentials/setup/)
- [جلب سجل](/core/tutorial/essentials/data-fetching/fetching-data/)
- [تحديث سجل](/core/tutorial/essentials/data-fetching/updating-data/)
- [عرض قائمة السجلات](/core/tutorial/essentials/data-fetching/listing-data/)
- [النماذج](/core/tutorial/essentials/forms/)
- [الجداول](/core/tutorial/essentials/tables/)

### المصادقة

- [مقدمة](/core/tutorial/authentication/intro/)
- [حماية المحتوى](/core/tutorial/authentication/protecting-content/)
- [تسجيل الدخول والخروج](/core/tutorial/authentication/logging-in-out/)
- [استخدام هوية المستخدم](/core/tutorial/authentication/user-identity/)
- [تكامل data provider](/core/tutorial/authentication/data-provider-integration/)

### التوجيه مع React Router

- [مقدمة](/core/tutorial/routing/intro/react-router/)
- [المصادقة](/core/tutorial/routing/authentication/react-router/)
- [تعريف resources](/core/tutorial/routing/resource-definition/react-router/)
- [التنقل](/core/tutorial/routing/navigation/react-router/)
- [استنتاج المعلمات](/core/tutorial/routing/inferring-parameters/react-router/)
- [إعادة التوجيه](/core/tutorial/routing/redirects/react-router/)
- [مزامنة الحالة مع الموقع](/core/tutorial/routing/syncing-state/react-router/)

### مكتبات الواجهة مع Ant Design

- [مقدمة](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [استخدام layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [إعادة الهيكلة](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [مكونات CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [الإشعارات](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [المصادقة](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### مكتبات الواجهة مع Material UI

- [مقدمة](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [استخدام layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [إعادة الهيكلة](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [مكونات CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [الإشعارات](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [المصادقة](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### الخطوات التالية مع Ant Design

- [مقدمة](/core/tutorial/next-steps/intro/ant-design/)
- [استخدام Inferencer](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [استخدام CLI](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [استخدام Devtools](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [الملخص](/core/tutorial/next-steps/summary/react-router/ant-design/)

### الخطوات التالية مع Material UI

- [مقدمة](/core/tutorial/next-steps/intro/material-ui/)
- [استخدام Inferencer](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [استخدام CLI](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [استخدام Devtools](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [الملخص](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
