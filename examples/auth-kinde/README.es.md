<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de autenticación con Kinde

Este ejemplo muestra cómo conectar **Refine** con Kinde para cubrir login, logout y lectura de identidad. La aplicación usa Kinde para la sesión y deja que Refine mantenga el flujo CRUD.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example auth-kinde
```

## Puntos clave

- Configuración de Kinde dentro del `authProvider`
- Flujo de sesión externo con resources de Refine
- Uso de identidad autenticada en las pantallas protegidas
- Comandos y nombres de API preservados en su forma original

[Abrir el ejemplo auth-kinde en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/auth-kinde?view=preview&theme=dark&codemirror=1)
