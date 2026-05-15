# Refine UI Tests

`@refinedev/ui-tests` contem utilitarios e cenarios de teste usados pelos pacotes de UI do Refine. Ele ajuda a validar comportamentos comuns entre diferentes integracoes de interface.

## Quando usar

Este pacote e voltado principalmente para manutencao interna e desenvolvimento dos pacotes de UI. Aplicacoes Refine comuns normalmente usam os pacotes publicos de UI, como `@refinedev/antd`, `@refinedev/mui`, `@refinedev/mantine` ou `@refinedev/chakra-ui`.

## Observacoes

- Mantenha nomes de componentes, props, fixtures e helpers iguais ao codigo.
- Use este pacote ao trabalhar em regressao visual, contratos de componentes ou suites compartilhadas.
- Consulte os scripts do workspace para executar os testes apropriados.
