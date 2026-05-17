<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de controle de acesso com Casbin

Este exemplo mostra como usar **refine** com Casbin para aplicar regras de autorizacao em recursos CRUD. O refine continua orquestrando resources e rotas, enquanto Casbin decide quais acoes cada usuario pode executar.

## Testar localmente

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## Pontos principais

- Integracao de Casbin com o `accessControlProvider`.
- Regras de permissao para acoes como list, create, edit e delete.
- Controle de acesso aplicado sem alterar os nomes de resources.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo access-control-casbin no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
