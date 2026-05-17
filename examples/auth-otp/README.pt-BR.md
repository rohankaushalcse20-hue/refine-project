<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao por OTP

Este exemplo mostra como usar **refine** em um fluxo de autenticacao com senha de uso unico. A aplicacao preserva o fluxo CRUD do refine e adiciona etapas especificas para validar o codigo OTP.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-otp
```

## Pontos principais

- Fluxo de login baseado em OTP.
- Uso de `authProvider` para validar credenciais e codigo.
- Redirecionamentos e rotas protegidas apos autenticacao.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo auth-otp no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
