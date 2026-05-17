<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de controle de acesso com Permify

Este exemplo mostra como usar **refine** com Permify para modelar permissoes em uma aplicacao React. O refine mantem o fluxo CRUD e consulta o provedor de acesso antes de liberar cada acao.

## Testar localmente

```bash
npm create refine-app@latest -- --example access-control-permify
```

## Pontos principais

- Integracao do Permify com o `accessControlProvider`.
- Regras por usuario, resource e operacao.
- UI protegida de acordo com as respostas de autorizacao.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo access-control-permify no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
