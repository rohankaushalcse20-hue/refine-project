<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Material UI 인증 예제

이 예제는 **Refine** 인증 흐름을 Material UI 기반 화면과 함께 구성하는 방법을 보여줍니다. 로그인 화면, 보호된 routes, resource 화면이 하나의 관리 UI로 연결됩니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example auth-material-ui
```

## 핵심 포인트

- Material UI 컴포넌트로 만든 인증 화면
- `authProvider`를 통한 로그인과 로그아웃 처리
- 인증 상태를 기반으로 한 routes 보호
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 auth-material-ui 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-material-ui?view=preview&theme=dark&codemirror=1)
