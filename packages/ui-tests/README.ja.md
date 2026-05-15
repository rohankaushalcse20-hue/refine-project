# Refine UI Tests

`@refinedev/ui-tests` は、refine の UI パッケージで使われる test utilities と test scenarios を含みます。複数の UI integration にまたがる共通のふるまいを検証するためのパッケージです。

## いつ使うか

このパッケージは主に UI パッケージの保守と開発向けです。一般的な refine アプリケーションでは、`@refinedev/antd`、`@refinedev/mui`、`@refinedev/mantine`、`@refinedev/chakra-ui` のような公開 UI パッケージを使います。

## 注意点

- component 名、props、fixtures、helpers はコードと同じ名前のまま扱います。
- visual regression、component contracts、shared suites を扱うときに使います。
- 適切な tests を実行するには workspace の scripts を確認してください。
