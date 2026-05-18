<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de control de acceso con Casbin

Este ejemplo muestra cómo usar **Refine** con Casbin para aplicar permisos en resources, acciones y rutas. Mantiene la lógica de autorización separada de la UI y deja que `accessControlProvider` decida qué puede ver o modificar cada usuario.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example access-control-casbin
```

## Puntos clave

- Integración de Casbin mediante `accessControlProvider`
- Reglas de autorización reutilizables para acciones CRUD
- Pantallas protegidas sin cambiar los nombres de resources de Refine
- Comandos, URLs y nombres técnicos conservados sin traducir

[Abrir el ejemplo access-control-casbin en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-casbin?view=preview&theme=dark&codemirror=1)
