# Herramientas codemod de Refine

`@refinedev/codemod` contiene transformaciones para actualizar proyectos Refine entre versiones y aplicar cambios mecanicos de API con menos trabajo manual.

## Instalacion y uso

Ejecuta el codemod desde la raiz de tu proyecto y revisa siempre el diff resultante antes de confirmar los cambios:

```sh
npx @refinedev/codemod
```

## Cuándo usarlo

Usa este paquete durante migraciones o actualizaciones grandes, especialmente cuando una version de Refine cambia imports, nombres de paquetes o patrones repetidos en muchos archivos.

## Documentacion

Consulta la [documentacion principal de Refine](https://refine.dev/docs/) y las notas de migracion correspondientes antes de ejecutar transformaciones sobre una rama compartida.
