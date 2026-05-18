<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de `useSelect` infinito com Ant Design

Este exemplo mostra como combinar **Refine**, `useSelect` e Ant Design para carregar opções paginadas em um campo `Select`. Ele é útil para listas grandes que não devem ser carregadas de uma vez.

## Executar localmente

```bash
npm create refine-app@latest -- --example field-antd-use-select-infinite
```

## Pontos principais

- Carregamento incremental de opções com `useSelect`
- Paginação conectada ao `dataProvider`
- Experiência melhor para relations com muitos registros
- Comandos, URLs e nomes de API preservados como no exemplo original

[Abrir o exemplo field-antd-use-select-infinite no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/field-antd-use-select-infinite?view=preview&theme=dark&codemirror=1)
