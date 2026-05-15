<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao com Kinde

Este exemplo mostra como integrar Kinde a uma aplicacao Refine. Ele usa um auth provider para lidar com login, logout, identidade do usuario e protecao de conteudo.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Pontos principais

- Configuracao do fluxo de autenticacao com Kinde.
- Paginas protegidas com base no estado de login.
- Identidade do usuario disponivel para a aplicacao Refine.
- Resources e rotas mantidos como nomes tecnicos do exemplo.

[Abrir o exemplo auth-kinde no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
