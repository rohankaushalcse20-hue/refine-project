<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ably live provider 예제

이 예제는 **Refine**에서 Ably를 live provider로 사용해 실시간 업데이트를 처리하는 방법을 보여줍니다. 데이터 변경이 발생하면 관련 resource 화면이 최신 상태를 반영합니다.

## 로컬에서 실행

```bash
npm create refine-app@latest -- --example live-provider-ably
```

## 핵심 포인트

- Ably 기반 live provider 구성
- publish와 subscribe 흐름으로 실시간 변경 반영
- Refine resources와 live event 연결
- 원본 명령어, URL, API 이름 유지

[CodeSandbox에서 live-provider-ably 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/live-provider-ably?view=preview&theme=dark&codemirror=1)
