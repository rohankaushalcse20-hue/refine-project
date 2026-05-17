<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de controle de acesso com Cerbos

Este exemplo mostra como conectar **refine** ao Cerbos para avaliar politicas de autorizacao em uma aplicacao CRUD. As telas e resources continuam no refine, enquanto o Cerbos fornece as decisoes de acesso.

## Testar localmente

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## Pontos principais

- Uso de Cerbos dentro do `accessControlProvider`.
- Verificacoes de permissao por resource e acao.
- Separacao entre regras de negocio e componentes de UI.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo access-control-cerbos no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
