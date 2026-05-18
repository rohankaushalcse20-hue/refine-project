<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de control de acceso con Permify

Este ejemplo muestra cómo integrar **Refine** con Permify para validar permisos basados en relaciones. Permify administra el modelo de autorización y Refine consume esas decisiones mediante `accessControlProvider`.

## Ejecutar en local

```bash
npm create refine-app@latest -- --example access-control-permify
```

## Puntos clave

- Autorización basada en relaciones con Permify
- Comprobaciones de acceso para resources y acciones
- Separación entre política, datos y componentes de UI
- Comandos, URLs y nombres técnicos conservados sin traducir

[Abrir el ejemplo access-control-permify en CodeSandbox](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/access-control-permify?view=preview&theme=dark&codemirror=1)
