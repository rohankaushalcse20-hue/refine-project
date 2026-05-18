<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Validación de formularios en servidor con Material UI

Este ejemplo muestra cómo propagar errores de validación de la API hacia campos Material UI en formularios administrados por Refine.

## Probar localmente

```bash
npm create refine-app@latest -- --example server-side-form-validation-material-ui
```

## Qué revisar

- Mapeo de errores remotos a inputs Material UI.
- Uso de `useForm` en pantallas create o edit.
- Estados de error y helper text por campo.
- Reintento después de corregir datos invalidos.

## CodeSandbox

[Abrir el ejemplo server-side-form-validation-material-ui](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/server-side-form-validation-material-ui?view=preview&theme=dark&codemirror=1)
