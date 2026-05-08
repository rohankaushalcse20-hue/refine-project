---
title: "Guía de bibliotecas UI | Buenas prácticas en Refine v5"
display_title: "Bibliotecas UI"
sidebar_label: "Bibliotecas UI"
description: "Aprende cómo funcionan las integraciones de UI en Refine v5 y cuándo conviene usar sus componentes, hooks y providers."
---

Las integraciones de bibliotecas UI de Refine amplían la funcionalidad principal al exponer hooks y componentes que aportan elementos visuales listos para usar con muy poca lógica adicional específica de cada librería. Refine ofrece integración fluida con bibliotecas UI populares para que elijas la que mejor encaje con tu proyecto. Estas integraciones no restringen la lógica de la aplicación: aunque aportan ventajas claras, puedes seguir creando, extendiendo o mezclando componentes por tu cuenta.

La arquitectura headless ofrece libertad para usar cualquier biblioteca UI o incluso crear una integración propia. La lógica de la aplicación queda encapsulada en hooks, helpers y componentes lógicos, por lo que sigue siendo agnóstica a la capa visual y altamente componible.

## Integraciones disponibles

Refine ofrece soporte listo para usar para cuatro bibliotecas muy utilizadas dentro del ecosistema React. Cada una incorpora su propia combinación de componentes y hooks, diseñados para integrarse con el menor esfuerzo posible.

Estas integraciones resuelven casos comunes como menús, layouts, botones de acción, tablas y formularios, manteniendo un lenguaje visual coherente con la biblioteca UI elegida. Más que una limitación, funcionan como extensiones y ayudas para las capacidades principales de Refine y de cada sistema de diseño.

- [Ant Design con `@refinedev/antd`](/core/docs/ui-integrations/ant-design/introduction/)
- [Material UI con `@refinedev/mui`](/core/docs/ui-integrations/material-ui/introduction/)
- [Chakra UI con `@refinedev/chakra-ui`](/core/docs/ui-integrations/chakra-ui/introduction/)
- [Mantine con `@refinedev/mantine`](/core/docs/ui-integrations/mantine/introduction/)

## Componentes preconstruidos

Los paquetes de integración UI de Refine exponen componentes preconstruidos pensados para trabajar con estas bibliotecas. Son composiciones entre la lógica de Refine y los componentes de la librería UI. Como su implementación se basa en esa librería, suelen ser fáciles de personalizar y ampliar según tus necesidades.

### Layouts y menús

Los layouts y los menús son elementos habituales en este tipo de aplicaciones, por eso ofrecemos componentes de layout y navegación para las bibliotecas UI compatibles. Aunque también combinan lógica del núcleo de Refine, se alinean con el lenguaje visual de cada librería y proporcionan una integración natural.

Estos componentes cubren las necesidades más comunes de una aplicación, pero mantienen suficiente flexibilidad para ajustarse a casos concretos. Por ejemplo, hay un componente `<Sider>` disponible en todas las integraciones UI, con menú de navegación multinivel, comprobaciones de autorización para las entradas del menú y un botón de logout que aprovecha el hook `useLogout` de Refine.

Como complemento del layout, también existe el componente `<Breadcrumb />`, pensado para mostrar navegación por migas en las vistas.

### Botones

Las integraciones UI de Refine ofrecen distintos botones construidos con los componentes adecuados de cada librería y con lógica adicional como comprobaciones de autorización, cuadros de confirmación, estados de carga, invalidación y navegación.

La lista de botones disponibles en las integraciones UI es:

- `<CreateButton />`
- `<EditButton />`
- `<ListButton />`
- `<ShowButton />`
- `<CloneButton />`
- `<DeleteButton />`
- `<SaveButton />`
- `<RefreshButton />`
- `<ImportButton />`
- `<ExportButton />`

### Vistas

Las vistas están diseñadas como envoltorios del contenido de las páginas de la aplicación. Se usan dentro de los layouts y aportan funcionalidades básicas como títulos basados en el resource, breadcrumbs, acciones relacionadas y comprobaciones de autorización.

La lista de vistas disponibles en las integraciones UI es:

- `<List />`
- `<Show />`
- `<Edit />`
- `<Create />`

### Campos

Los componentes de campo permiten renderizar valores con el diseño y formato adecuados para la biblioteca UI. Se construyen sobre los componentes nativos de cada librería y añaden lógica de formateo. Aunque en algunos casos quizá no cubran por completo tu necesidad, se pueden combinar o ampliar para lograr el comportamiento esperado.

La lista de componentes de campo incluidos es:

- `<BooleanField />`
- `<DateField />`
- `<EmailField />`
- `<FileField />`
- `<ImageField />`
- `<MarkdownField />`
- `<NumberField />`
- `<TagsField />`
- `<TextField />`
- `<UrlField />`

### Páginas de autenticación

Las páginas de autenticación están pensadas para cubrir el flujo de acceso de la aplicación. Ofrecen una solución lista para usar para login, registro, recuperación y restablecimiento de contraseña aprovechando los hooks de autenticación de Refine.

Los tipos de páginas de autenticación disponibles en las integraciones UI son:

- `<AuthPage type="login" />`
- `<AuthPage type="register" />`
- `<AuthPage type="forgot-password" />`
- `<AuthPage type="reset-password" />`

### Páginas de error

Las integraciones UI de Refine también ofrecen un componente `<ErrorPage />` que puedes usar para mostrar una página 404 en tu aplicación. Aunque no añade mucha lógica, es una forma rápida de mantener un diseño coherente también en las pantallas de error.

## Personalización

Aunque los componentes exportados por las integraciones UI suelen aceptar los props del componente subyacente de cada librería, en algunos casos puede que necesites personalizarlos tanto a nivel lógico como visual. Para ello tienes varias opciones, desde la más simple hasta la más avanzada:

### Usar los props

En muchos de estos componentes puedes pasar props para sobrescribir o extender el estilo y la lógica existentes. Es el enfoque más sencillo, aunque a veces se queda corto. Por ejemplo, si quieres ocultar `<EditButton />` en lugar de deshabilitarlo según la autorización del usuario, puedes pasar el prop `accessControl` al componente.

```tsx title="edit.tsx"
import { EditButton } from "@refinedev/antd";

<EditButton
  accessControl={{
    hideIfUnauthorized: true,
  }}
/>;
```

### Usar las opciones de Refine

Refine permite cambiar algunas configuraciones de componentes y hooks globalmente a través del componente `<Refine>`. Así puedes modificar el comportamiento lógico y visual predeterminado de los componentes UI. Por ejemplo, podemos cambiar la visibilidad de los botones según el estado de autorización directamente desde `<Refine>`.

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";

<Refine
    accessControlProvider={{
        can: async ({ resource, action, params }) => { ... },
        options: {
            buttons: {
                hideIfUnauthorized: true,
            },
        },
    }}
/>
```

[Para conocer más opciones, consulta la documentación del componente `<Refine>`.](/core/docs/core/refine-component/)

### Usar el comando `swizzle`

La CLI de Refine incluye un comando llamado `swizzle` que te permite exportar componentes de las integraciones UI para usarlos dentro de tu aplicación. Esto te deja modificar cada componente con mayor granularidad. Por ejemplo, puedes exportar `<EditButton />` y ajustar su lógica para ocultarlo en lugar de deshabilitarlo.

```bash
> npm run refine swizzle

Which package do you want to swizzle? (Use arrow keys or type to search)

Data Provider
 ◯ @refinedev/simple-rest
UI Framework
 ◉ @refinedev/antd

Which component do you want to swizzle?

Buttons
 ◯ CreateButton
 ◯ ShowButton
❯◉ EditButton
Pages
 ◯ ErrorPage
 ◯ AuthPage

(Move up and down to reveal more choices)
```

[Para conocer más sobre `swizzle`, consulta la documentación de la CLI.](/core/docs/packages/list-of-packages/)

> Aunque `swizzle` ofrece una vía para personalizar componentes, es una operación puntual y puede resultar más difícil mantener esos cambios y seguir las nuevas funcionalidades en el futuro. Al hacer swizzle de un componente, lo desacoplas del paquete original y pasas a ser responsable de mantenerlo al día.

## Notificaciones <GuideBadge id="guides-concepts/notifications/" />

Una parte importante de cualquier aplicación son las notificaciones y la retroalimentación visual. Refine incluye una integración de notificaciones que funciona automáticamente cuando hace falta, por ejemplo cuando falla una petición o cuando se envía un formulario.

Aunque esta integración no está acoplada a las bibliotecas UI, suele ser buena idea usar la implementación que ofrece tu librería visual para mantener un lenguaje de diseño consistente. Por eso las integraciones UI de Refine también exponen un `notificationProvider` pensado para trabajar con el sistema de notificaciones de cada librería.

Usar estos notification providers preconstruidos es opcional: puedes personalizarlos, extenderlos o incluso sustituirlos por una implementación propia.

```tsx title="App.tsx"
import { Refine } from "@refinedev/core";
import { useNotificationProvider } from "@refinedev/mantine";

const App = () => (
  <Refine
    // highlight-next-line
    notificationProvider={useNotificationProvider}
    /* ... */
  >
    {/* ... */}
  </Refine>
);
```

## Implementaciones personalizadas

Aunque existen integraciones para las bibliotecas UI más populares, cada aplicación tiene necesidades y restricciones propias. Por eso Refine está diseñado para trabajar con cualquier biblioteca UI o incluso sin ninguna. Lo mismo ocurre con las integraciones UI: puedes construir tu propia integración si eso encaja mejor con tu caso.

Si decides crear una integración UI personalizada, el código fuente de las integraciones existentes es un buen punto de partida. Puedes revisar ese código en el [repositorio de GitHub](https://github.com/refinedev/refine).
