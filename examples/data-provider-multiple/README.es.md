<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo con múltiples data providers

Este ejemplo muestra cómo trabajar con varios data providers dentro de una misma aplicación Refine cuando distintos recursos usan backends diferentes.

## Probar localmente

```bash
npm create refine-app@latest -- --example data-provider-multiple
```

## Qué revisar

- Asignación de un provider por resource.
- Uso de `dataProviderName` en operaciónes concretas.
- Navegacion entre recursos con orígenes de datos distintos.
- Separación clara de endpoints y credenciales.

## CodeSandbox

[Abrir el ejemplo data-provider-multiple](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/data-provider-multiple?view=preview&theme=dark&codemirror=1)
