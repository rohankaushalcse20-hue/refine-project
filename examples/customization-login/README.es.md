<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de login personalizado

Este ejemplo muestra cómo reemplazar la pantalla de login por una experiencia propia sin cambiar el contrato de autenticación de Refine.

## Probar localmente

```bash
npm create refine-app@latest -- --example customization-login
```

## Qué revisar

- Composicion de una pagina de login personalizada.
- Conexión con `authProvider` para iniciar sesión.
- Estados de error y carga durante el acceso.
- Mantenimiento de rutas protegidas después del login.

## CodeSandbox

[Abrir el ejemplo customization-login](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/customization-login?view=preview&theme=dark&codemirror=1)
