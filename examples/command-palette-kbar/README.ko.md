<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## kbar Command Palette 예제

이 예제는 **Refine** 애플리케이션에 kbar 기반 command palette를 연결하는 방법을 보여줍니다. 사용자는 keyboard 중심으로 resource 이동과 주요 action을 실행할 수 있습니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example command-palette-kbar
```

## 확인할 점

- kbar command palette와 Refine navigation 연결
- resource별 action을 command로 노출하는 방식
- keyboard workflow와 route 이동 흐름
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 command-palette-kbar 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/command-palette-kbar?view=preview&theme=dark&codemirror=1)
