<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Keycloak 인증 예제

이 예제는 **Refine**을 Keycloak과 통합해 세션, 권한, 사용자 식별을 외부 provider에서 관리하는 방법을 보여줍니다. Refine은 resources, routes, 관리 화면을 계속 조율합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## 핵심 포인트

- Keycloak을 `authProvider` 안에 통합
- login, logout, 사용자 식별 처리
- 인증 상태를 기준으로 routes 보호
- 원본 API 이름, 명령어, URL 유지

[CodeSandbox에서 auth-keycloak 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
