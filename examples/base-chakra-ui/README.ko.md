<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Chakra UI 기본 예제

이 예제는 **Refine** 애플리케이션을 Chakra UI 컴포넌트와 함께 시작하는 방법을 보여줍니다. headless CRUD 로직은 Refine에 맡기고, 화면 구성과 스타일은 Chakra UI로 처리합니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example base-chakra-ui
```

## 확인할 점

- Chakra UI 컴포넌트로 구성한 기본 resource 화면
- `dataProvider`를 사용한 목록, 생성, 수정 흐름
- Refine routing과 layout 연결
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 base-chakra-ui 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-chakra-ui?view=preview&theme=dark&codemirror=1)
