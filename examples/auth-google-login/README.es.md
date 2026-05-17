<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de autenticación con Google Login

Este ejemplo muestra cómo usar **Refine** con un proveedor de login de Google. El flujo mantiene la lógica de autenticación separada del CRUD para que los resources sigan usando los providers habituales.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example auth-google-login
```

## Puntos clave

- Configuración de `authProvider` para Google Login
- Lectura de identidad de usuario después del inicio de sesión
- Protección de vistas y resources con el estado autenticado
- Comandos, URLs y nombres técnicos sin traducir

[Abrir el ejemplo auth-google-login en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-google-login?view=preview&theme=dark&codemirror=1)
