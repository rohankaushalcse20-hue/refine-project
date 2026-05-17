<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo com multiplos data providers

Este exemplo mostra como usar **refine** com mais de um data provider na mesma aplicacao. Cada resource pode apontar para a fonte de dados correta sem perder o fluxo CRUD padrao.

## Testar localmente

```bash
npm create refine-app@latest -- --example data-provider-multiple
```

## Pontos principais

- Configuracao de varios `dataProvider`.
- Resources conectados a fontes de dados diferentes.
- Reuso dos hooks CRUD do refine em cada provider.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo data-provider-multiple no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-multiple?view=preview&theme=dark&codemirror=1)
