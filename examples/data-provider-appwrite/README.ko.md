<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Appwrite data provider 예제

이 예제는 **Refine**을 Appwrite backend와 연결하는 방법을 보여줍니다. Appwrite collections를 Refine resources로 다루면서 목록, 생성, 수정 흐름을 유지합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example data-provider-appwrite
```

## 핵심 포인트

- Appwrite data provider 설정
- collections와 resources 사이의 CRUD 매핑
- 인증과 데이터 접근을 backend provider에 위임
- 원본 예제의 명령어, URL, API 이름 유지

[CodeSandbox에서 data-provider-appwrite 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-appwrite?view=preview&theme=dark&codemirror=1)
