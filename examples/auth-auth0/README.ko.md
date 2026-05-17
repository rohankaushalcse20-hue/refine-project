<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Auth0 인증 예제

이 예제는 **Refine**을 Auth0 로그인 흐름과 연결하는 방법을 보여줍니다. Refine의 resources와 providers 구조는 유지하면서 사용자 식별과 세션 처리는 Auth0가 담당합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example auth-auth0
```

## 핵심 포인트

- Auth0와 `authProvider` 통합
- 인증된 routes와 resources 보호
- 외부 로그인 흐름을 Refine 구조에 연결
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 auth-auth0 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
