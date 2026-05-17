<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Google 로그인 인증 예제

이 예제는 **Refine** 애플리케이션에 Google 로그인을 붙이는 방법을 보여줍니다. Google 계정으로 사용자를 인증하고, Refine의 resource 기반 화면은 기존 구조대로 유지합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example auth-google-login
```

## 핵심 포인트

- Google 로그인 흐름과 `authProvider` 연결
- 로그인 상태에 따른 페이지 접근 제어
- 사용자 정보와 세션 상태 처리
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 auth-google-login 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
