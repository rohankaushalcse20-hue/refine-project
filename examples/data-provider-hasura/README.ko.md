<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Hasura data provider 예제

이 예제는 **Refine**이 Hasura GraphQL API를 data provider로 사용하는 방법을 보여줍니다. Refine resources가 GraphQL query와 mutation으로 연결되어 관리 화면을 구성합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example data-provider-hasura
```

## 핵심 포인트

- Hasura GraphQL endpoint와 data provider 연결
- resources를 query와 mutation 흐름에 매핑
- 목록, 상세, 생성, 수정 작업 처리
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 data-provider-hasura 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-hasura?view=preview&theme=dark&codemirror=1)
