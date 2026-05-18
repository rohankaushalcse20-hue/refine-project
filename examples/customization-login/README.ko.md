<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Custom Login 예제

이 예제는 **Refine** 인증 흐름에서 로그인 화면을 직접 커스터마이징하는 방법을 보여줍니다. `authProvider`와 보호된 routes는 유지하면서 브랜드와 입력 UI를 프로젝트에 맞게 조정할 수 있습니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example customization-login
```

## 확인할 점

- custom login page와 `authProvider` 연결
- 인증 상태에 따른 routes 보호
- 로그인 화면의 copy, layout, form 구성 변경
- 명령어, URL, API 이름은 원본 그대로 유지

[CodeSandbox에서 customization-login 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-login?view=preview&theme=dark&codemirror=1)
