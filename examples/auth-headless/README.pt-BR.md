<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de autenticacao headless

Este exemplo mostra como implementar autenticacao com **refine** sem depender de uma biblioteca de UI especifica. A logica de autenticacao fica no refine, e a interface pode ser adaptada para qualquer design system.

## Testar localmente

```bash
npm create refine-app@latest -- --example auth-headless
```

## Pontos principais

- Configuracao headless de `authProvider`.
- Rotas protegidas e redirecionamentos de autenticacao.
- Separacao entre logica de acesso e componentes visuais.
- Comandos, URLs e APIs preservados no codigo.

[Abrir o exemplo auth-headless no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-headless?view=preview&theme=dark&codemirror=1)
