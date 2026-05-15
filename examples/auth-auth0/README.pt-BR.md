<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao com Auth0

Este exemplo mostra como conectar **refine** a um fluxo de login com Auth0. A aplicacao continua usando os recursos e providers do refine, enquanto a identidade do usuario e gerenciada pelo provedor Auth0.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Pontos principais

- Integracao de `authProvider` com Auth0.
- Protecao de rotas e recursos autenticados.
- Fluxo de login externo preservando a estrutura do refine.
- Comandos e URLs mantidos como no exemplo original.

[Abrir o exemplo auth-auth0 no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
