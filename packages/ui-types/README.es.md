# Tipos de UI de Refine

`@refinedev/ui-types` contiene tipos compartidos para las integraciones de UI de Refine. Ayuda a mantener contratos consistentes entre paquetes como Ant Design, Material UI, Mantine y Chakra UI.

## Para que sirve

Refine es headless: la logica de datos, routing, autenticacion, autorizacion, notificaciones e i18n vive separada de la capa visual. Este paquete centraliza tipos que las integraciones visuales pueden reutilizar sin duplicar contratos.

## Uso habitual

Normalmente no necesitas instalar `@refinedev/ui-types` directamente en una aplicacion. Se consume como dependencia interna de otros paquetes `@refinedev/*`.

## Casos de uso

- Mantener APIs de componentes alineadas entre integraciones de UI.
- Compartir contratos TypeScript para acciones, props y estados visuales.
- Facilitar contribuciones a paquetes de UI dentro del monorepo de Refine.

## Documentacion

Consulta la [documentacion principal de Refine](https://refine.dev/docs/) para entender como se relacionan los paquetes de UI con el core headless.
