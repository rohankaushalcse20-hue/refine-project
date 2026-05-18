<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Headless 기본 예제

이 예제는 특정 UI 라이브러리에 묶이지 않고 **Refine**의 핵심 hook과 provider를 사용하는 기본 구성을 보여줍니다. 자체 UI를 만들면서도 resource, routing, data fetching 흐름은 Refine 구조를 따릅니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example base-headless
```

## 확인할 점

- UI 프레임워크 없이 사용하는 Refine CRUD 흐름
- `useTable`, `useForm` 같은 핵심 hook의 역할
- `resources`, routes, `dataProvider`의 연결 방식
- code 안의 API 이름과 명령어는 원본 그대로 유지

[CodeSandbox에서 base-headless 예제 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/base-headless?view=preview&theme=dark&codemirror=1)
