<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Mantine Theme 커스터마이징 예제

이 예제는 **Refine**와 Mantine을 함께 사용할 때 theme 값을 정의하고 애플리케이션 전체에 적용하는 방법을 보여줍니다. CRUD 동작은 Refine에 유지하고, 시각 스타일은 Mantine theme로 관리합니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example customization-theme-mantine
```

## 확인할 점

- Mantine theme provider 설정
- resource 화면에 공통 theme가 적용되는 흐름
- 색상, spacing, component 기본값 조정
- 명령어, URL, API 이름은 원본 그대로 유지

[CodeSandbox에서 customization-theme-mantine 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-theme-mantine?view=preview&theme=dark&codemirror=1)
