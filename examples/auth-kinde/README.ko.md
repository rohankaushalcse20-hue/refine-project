<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Kinde 인증 예제

이 예제는 **Refine** 프로젝트에서 Kinde를 인증 provider로 사용하는 방법을 보여줍니다. Kinde가 사용자 로그인과 세션을 처리하고, Refine은 인증된 resources를 렌더링합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example auth-kinde
```

## 핵심 포인트

- Kinde 기반 `authProvider` 구성
- 인증 상태에 따른 resource 접근 제어
- 사용자 세션과 리다이렉트 흐름 처리
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 auth-kinde 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
