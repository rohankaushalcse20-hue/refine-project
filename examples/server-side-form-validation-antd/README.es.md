<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Validación de formularios en servidor con Ant Design

Este ejemplo muestra cómo presentar errores de validación devueltos por el servidor dentro de formularios creados con Ant Design y Refine.

## Probar localmente

```bash
npm create refine-app@latest -- --example server-side-form-validation-antd
```

## Qué revisar

- Mapeo de errores del backend a campos de Ant Design.
- Flujo de envío con `useForm`.
- Mensajes de error junto a cada campo afectado.
- Comportamiento cuando la API rechaza datos invalidos.

## CodeSandbox

[Abrir el ejemplo server-side-form-validation-antd](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/server-side-form-validation-antd?view=preview&theme=dark&codemirror=1)
