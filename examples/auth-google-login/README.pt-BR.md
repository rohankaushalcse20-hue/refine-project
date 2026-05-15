<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao com Google Login

Este exemplo mostra como usar **refine** com login pelo Google. Ele demonstra como integrar um provedor de identidade externo ao fluxo de autenticacao sem alterar os resources e as rotas principais da aplicacao.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Pontos principais

- Login com conta Google.
- Uso de `authProvider` no fluxo do refine.
- Rotas protegidas para conteudo autenticado.
- Nomes de exemplo, comandos e APIs preservados.

[Abrir o exemplo auth-google-login no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
