# Template registry-template

Voce pode usar a CLI `shadcn` para executar seu proprio registro de componentes. Ter um registro proprio permite distribuir componentes, hooks, paginas e outros arquivos personalizados para qualquer projeto React.

> [!IMPORTANT]
> Este template usa Tailwind v4. Para Tailwind v3, consulte [registry-template](https://github.com/shadcn-ui/registry-template).

## Primeiros passos

Este e um template para criar um registro personalizado com Next.js.

- O template usa um arquivo `registry.json` para definir componentes e seus arquivos.
- O comando `shadcn build` e usado para construir o registro.
- Os itens do registro sao servidos como arquivos estaticos em `public/r/[name].json`.
- O template tambem inclui um route handler para servir itens do registro.
- Todos os itens do registro sao compativeis com a CLI `shadcn`.
- Tambem ha integracao com v0 por meio da API `Open in v0`.

## Documentacao

Visite a [documentacao do shadcn](https://ui.shadcn.com/docs/registry) para ver a documentacao completa.
