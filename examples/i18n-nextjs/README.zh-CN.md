<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Next.js 的 i18n 示例

这个 example 展示了如何把 **Refine**、Next.js 与国际化组合起来，让 routes、rendering 与内容都能跟随用户的 locale 设置工作。

## 本地运行

```bash
npm create refine-app@latest -- --example i18n-nextjs
```

## 关键点

- Next.js 的 locales 配置
- 将 `i18nProvider` 接入 `<Refine />`
- navigation 与 CRUD actions 的翻译
- 与 Next.js routing、rendering 流程的兼容方式

[打开 i18n-nextjs example](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/i18n-nextjs?view=preview&theme=dark&codemirror=1)
