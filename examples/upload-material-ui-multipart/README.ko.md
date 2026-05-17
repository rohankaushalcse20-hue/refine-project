<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Material UI multipart 업로드 예제

이 예제는 **Refine**과 Material UI로 multipart 파일 업로드 흐름을 구성하는 방법을 보여줍니다. form submit 과정에서 파일 입력을 resource mutation과 함께 처리합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example upload-material-ui-multipart
```

## 핵심 포인트

- Material UI form에서 파일 입력 처리
- multipart upload를 resource mutation에 연결
- 업로드 상태와 form submit 흐름 관리
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 upload-material-ui-multipart 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/upload-material-ui-multipart?view=preview&theme=dark&codemirror=1)
