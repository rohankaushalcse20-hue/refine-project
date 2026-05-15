# Plantilla registry-template

Puedes usar la CLI de `shadcn` para ejecutar tu propio registro de componentes. Tener un registro propio te permite distribuir componentes, hooks, paginas y otros archivos personalizados a cualquier proyecto React.

> [!IMPORTANT]
> Esta plantilla usa Tailwind v4. Para Tailwind v3, consulta [registry-template](https://github.com/shadcn-ui/registry-template).

## Primeros pasos

Esta es una plantilla para crear un registro personalizado con Next.js.

- La plantilla usa un archivo `registry.json` para definir componentes y sus archivos.
- El comando `shadcn build` se usa para construir el registro.
- Los items del registro se sirven como archivos estaticos bajo `public/r/[name].json`.
- La plantilla tambien incluye un route handler para servir items del registro.
- Cada item del registro es compatible con la CLI de `shadcn`.
- Tambien se incluye integracion con v0 mediante la API `Open in v0`.

## Documentacion

Visita la [documentacion de shadcn](https://ui.shadcn.com/docs/registry) para ver la documentacion completa.
