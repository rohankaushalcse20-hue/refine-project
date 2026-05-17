<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de autenticación con Auth0

Este ejemplo muestra cómo conectar **Refine** con un flujo de inicio de sesión de Auth0. La aplicación conserva los resources y providers de Refine, mientras Auth0 gestiona la identidad del usuario.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example auth-auth0
```

## Puntos clave

- Integración de `authProvider` con Auth0
- Rutas protegidas y resources autenticados
- Flujo de login externo sin cambiar la estructura de Refine
- Comandos, URLs y nombres de API conservados como en el ejemplo original

[Abrir el ejemplo auth-auth0 en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-auth0?view=preview&theme=dark&codemirror=1)
