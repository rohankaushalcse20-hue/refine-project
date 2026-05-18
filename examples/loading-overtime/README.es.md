<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de loading overtime

Este ejemplo muestra cómo manejar estados de carga prolongados en Refine para dar contexto al usuario cuando una operación tarda mas de lo esperado.

## Probar localmente

```bash
npm create refine-app@latest -- --example loading-overtime
```

## Qué revisar

- Uso de `overtimeOptions` en operaciónes asíncronas.
- Mensajes visibles cuando la carga supera el umbral configurado.
- Coordinación con estados de loading existentes.
- Experiencia de usuario para solicitudes lentas.

## CodeSandbox

[Abrir el ejemplo loading-overtime](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/loading-overtime?view=preview&theme=dark&codemirror=1)
