<div align="center" style="margin: 30px;">
<a href="https://refine.dev/">
  <img alt="refine logo" src="https://refine.ams3.cdn.digitaloceanspaces.com/readme/refine-readme-banner.png">
</a>
</div>

## Ejemplo de audit log provider

Este ejemplo muestra cómo conectar un `auditLogProvider` en una aplicación Refine para registrar acciones de recursos sin cambiar el flujo CRUD principal.

## Probar localmente

```bash
npm create refine-app@latest -- --example audit-log-provider
```

## Qué revisar

- Registro de acciones de create, update y delete.
- Integración del provider con `<Refine />`.
- Revisión de payloads enviados al servicio de auditoría.
- Conservación de nombres de resources y métodos del provider.

## CodeSandbox

[Abrir el ejemplo audit-log-provider](https://codesandbox.io/embed/github/refinedev/refine/tree/main/examples/audit-log-provider?view=preview&theme=dark&codemirror=1)
