---
title: 導入
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

このチュートリアルでは、Refine の基本から応用までを段階的にたどります。最終的には、Refine を使った本格的な CRUD アプリケーションの構築フローを一通り体験できます。

Refine は router 非依存なので、慣れているルーティングライブラリを選べます。Refine は [React Router DOM](/core/docs/routing/integrations/react-router)、[Next.js](/core/docs/routing/integrations/next-js)、[Remix](/core/docs/routing/integrations/remix) を公式にサポートしています。以降のチュートリアルでは、選択した routing に応じた内容が表示されます。途中で選択を切り替えて、ほかのライブラリ向けの内容を確認することもできます。

続ける routing ライブラリを選択してください。

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

この後のユニットでは、Refine の UI integration も選択し、それらがどのように構築され、どのような場面で役立つかを学びます。Refine は Ant Design、Material UI、Mantine、Chakra UI を公式にサポートしていますが、このチュートリアルでは特に利用者の多い [Ant Design](/core/docs/ui-integrations/ant-design/introduction) と [Material UI](/core/docs/ui-integrations/material-ui/introduction) を扱います。

続ける UI framework を選択してください。

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

ほかの UI ライブラリ向けの内容は、[ドキュメント](/core/docs/guides-concepts/ui-libraries) で確認できます。

## チュートリアルの内容

以下に、トピックごとに整理されたチュートリアルの各セクションを示します。

### 基礎

- [最初の Refine アプリ](/core/tutorial/essentials/setup/)
- [レコードを取得する](/core/tutorial/essentials/data-fetching/fetching-data/)
- [レコードを更新する](/core/tutorial/essentials/data-fetching/updating-data/)
- [レコードを一覧表示する](/core/tutorial/essentials/data-fetching/listing-data/)
- [フォーム](/core/tutorial/essentials/forms/)
- [テーブル](/core/tutorial/essentials/tables/)

### 認証

- [導入](/core/tutorial/authentication/intro/)
- [コンテンツを保護する](/core/tutorial/authentication/protecting-content/)
- [ログインとログアウト](/core/tutorial/authentication/logging-in-out/)
- [ユーザー identity を使う](/core/tutorial/authentication/user-identity/)
- [data provider との統合](/core/tutorial/authentication/data-provider-integration/)

### React Router でのルーティング

- [導入](/core/tutorial/routing/intro/react-router/)
- [認証](/core/tutorial/routing/authentication/react-router/)
- [resources を定義する](/core/tutorial/routing/resource-definition/react-router/)
- [ナビゲーション](/core/tutorial/routing/navigation/react-router/)
- [パラメータを推論する](/core/tutorial/routing/inferring-parameters/react-router/)
- [リダイレクト](/core/tutorial/routing/redirects/react-router/)
- [URL と state を同期する](/core/tutorial/routing/syncing-state/react-router/)

### Ant Design と UI ライブラリ

- [導入](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [layouts を使う](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [リファクタリング](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [CRUD components](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [通知](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [認証](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Material UI と UI ライブラリ

- [導入](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [layouts を使う](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [リファクタリング](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [CRUD components](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [通知](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [認証](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Ant Design の次のステップ

- [導入](/core/tutorial/next-steps/intro/ant-design/)
- [Inferencer を使う](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [CLI を使う](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Devtools を使う](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [まとめ](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Material UI の次のステップ

- [導入](/core/tutorial/next-steps/intro/material-ui/)
- [Inferencer を使う](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [CLI を使う](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Devtools を使う](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [まとめ](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
