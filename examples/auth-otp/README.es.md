<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de autenticación con OTP

Este ejemplo muestra cómo implementar un flujo de inicio de sesión con contraseña de un solo uso en **Refine**. La lógica de identidad vive en `authProvider`, mientras la aplicación mantiene rutas protegidas y resources autenticados.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example auth-otp
```

## Puntos clave

- Flujo de login basado en OTP
- Validación de sesión mediante `authProvider`
- Rutas protegidas para usuarios autenticados
- Comandos, URLs y nombres de API conservados como en el ejemplo original

[Abrir el ejemplo auth-otp en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-otp?view=preview&theme=dark&codemirror=1)
