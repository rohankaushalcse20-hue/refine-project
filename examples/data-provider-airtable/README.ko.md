<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Airtable data provider 예제

이 예제는 Airtable을 backend로 사용해 **Refine** resources를 연결하는 방법을 보여줍니다. data provider가 Refine의 CRUD 흐름과 Airtable bases 사이의 통신을 담당합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example data-provider-airtable
```

## 핵심 포인트

- Airtable을 data provider로 구성
- Refine resources에서 records 읽기와 쓰기
- UI, resources, 데이터 접근 계층 분리
- 명령어, URL, 기술 이름은 번역하지 않고 유지

[CodeSandbox에서 data-provider-airtable 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-airtable?view=preview&theme=dark&codemirror=1)
