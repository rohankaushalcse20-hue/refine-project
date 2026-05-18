<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine 기본 예제

이 예제는 **Refine**의 CRUD 구조를 Mantine 기반 화면과 함께 구성하는 방법을 보여줍니다. resource 정의와 data fetching은 Refine이 담당하고, form과 layout 표현은 Mantine 컴포넌트로 처리합니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example base-mantine
```

## 확인할 점

- Mantine 컴포넌트로 만든 기본 CRUD 화면
- `dataProvider`와 resource 기반 navigation
- list, create, edit 흐름의 연결
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 base-mantine 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-mantine?view=preview&theme=dark&codemirror=1)
