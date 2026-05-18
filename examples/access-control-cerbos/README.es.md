<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de control de acceso con Cerbos

Este ejemplo muestra cómo conectar **Refine** con Cerbos para evaluar políticas de autorización desde un servicio externo. La aplicación conserva los resources y acciones de Refine mientras Cerbos responde si una operación está permitida.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example access-control-cerbos
```

## Puntos clave

- Uso de Cerbos como motor de políticas
- Decisiones de acceso centralizadas para vistas y acciones CRUD
- Integración con `accessControlProvider`
- Comandos, URLs y nombres de API conservados como en el ejemplo original

[Abrir el ejemplo access-control-cerbos en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-cerbos?view=preview&theme=dark&codemirror=1)
