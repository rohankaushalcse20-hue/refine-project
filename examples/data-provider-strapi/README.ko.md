<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Strapi data provider 예제

이 예제는 **Refine**을 Strapi backend와 함께 사용하는 방법을 보여줍니다. Strapi content type을 Refine resources로 노출해 관리 화면에서 CRUD 작업을 수행합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example data-provider-strapi
```

## 핵심 포인트

- Strapi REST API와 data provider 연결
- content type을 Refine resources로 관리
- 목록, 생성, 수정, 삭제 흐름 구성
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 data-provider-strapi 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-strapi?view=preview&theme=dark&codemirror=1)
