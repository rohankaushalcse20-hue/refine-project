<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de autenticación con Keycloak

Este ejemplo muestra cómo integrar **Refine** con Keycloak para gestionar sesiones, permisos e identidad desde un proveedor externo. Refine sigue coordinando los resources, rutas y pantallas de administración.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example auth-keycloak
```

## Puntos clave

- Integración de Keycloak dentro de `authProvider`
- Manejo de login, logout e identidad del usuario
- Protección de rutas con el estado de autenticación
- Conservación de nombres de APIs, comandos y URLs originales

[Abrir el ejemplo auth-keycloak en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-keycloak?view=preview&theme=dark&codemirror=1)
