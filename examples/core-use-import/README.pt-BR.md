<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Exemplo de `useImport`

Este exemplo mostra como o **Refine** usa `useImport` para importar registros a partir de arquivos. O fluxo conecta os dados importados ao `dataProvider` sem alterar a estrutura dos resources.

## Executar localmente

```bash
npm create refine-app@latest -- --example core-use-import
```

## Pontos principais

- Importação de arquivos com o hook `useImport`
- Envio de registros importados para o `dataProvider`
- Estados de sucesso e erro durante o processo
- Comandos, URLs e nomes de API preservados como no exemplo original

[Abrir o exemplo core-use-import no CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/core-use-import?view=preview&theme=dark&codemirror=1)
