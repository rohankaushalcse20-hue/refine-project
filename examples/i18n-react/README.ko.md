<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## React용 i18n 예제

이 example은 **Refine**를 React 애플리케이션에서 국제화와 함께 사용하는 방법을 보여 줍니다. CRUD 로직은 Refine에 맡기고, 번역은 적절한 provider를 통해 추가합니다.

## 로컬에서 실행하기

```bash
npm create refine-app@latest -- --example i18n-react
```

## 확인할 점

- `i18nProvider` 설정 방식
- UI에서 언어를 전환하는 흐름
- menus, actions, 표시 텍스트 번역
- code 안의 resources, routes, APIs가 그대로 유지되는지 확인

[i18n-react example 열기](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-react?view=preview&theme=dark&codemirror=1)
