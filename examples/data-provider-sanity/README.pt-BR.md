<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de Data Provider com Sanity

Este exemplo mostra como conectar o **Refine** ao Sanity por meio de um `dataProvider`. As telas CRUD continuam usando resources do Refine enquanto o provider traduz as operações para a API do Sanity.

## Executar localmente

```bash
npm create refine-app@latest -- --example data-provider-sanity
```

## Pontos principais

- Integração com Sanity via `dataProvider`
- Operações CRUD conectadas aos resources
- Separação entre UI, resources e camada de dados
- Comandos, URLs e nomes de API preservados como no exemplo original

[Abrir o exemplo data-provider-sanity no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-sanity?view=preview&theme=dark&codemirror=1)
