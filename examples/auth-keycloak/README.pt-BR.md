<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao com Keycloak

Este exemplo demonstra como usar Keycloak como auth provider em uma aplicacao Refine. Ele cobre o fluxo de login, logout e protecao de paginas mantendo a configuracao de resources separada da camada de autenticacao.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Pontos principais

- Integracao de um auth provider baseado em Keycloak.
- Rotas protegidas para areas autenticadas.
- Tratamento de sessao sem alterar nomes de APIs ou variaveis do exemplo.
- Base para adaptar roles e permissoes do Keycloak ao Refine.

[Abrir o exemplo auth-keycloak no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
