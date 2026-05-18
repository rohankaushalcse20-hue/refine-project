<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Top Menu Layout 예제

이 예제는 **Refine**의 navigation을 sider 대신 상단 메뉴 중심으로 구성하는 방법을 보여줍니다. resource 기반 route 구조는 유지하면서 desktop 화면에 맞는 top menu layout을 적용합니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example customization-top-menu-layout
```

## 확인할 점

- top menu layout과 resource navigation 연결
- list, create, edit routes의 이동 흐름
- sider 없는 화면에서 메뉴 상태를 관리하는 방식
- 명령어, URL, API 이름은 원본 그대로 유지

[CodeSandbox에서 customization-top-menu-layout 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-top-menu-layout?view=preview&theme=dark&codemirror=1)
