---
title: Introducción
---

import { Sandpack } from "./sandpack.tsx";
import { TutorialParameterDropdown } from "@site/src/refine-theme/tutorial-parameter-dropdown";

<Sandpack>

Este tutorial te llevará desde los fundamentos de Refine hasta temas más avanzados. Aprenderás a construir una aplicación CRUD completa con Refine.

Refine es agnóstico al router, así que puedes elegir la librería de rutas con la que te sientas más cómodo. Refine ofrece soporte oficial para [React Router DOM](/core/docs/routing/integrations/react-router), [Next.js](/core/docs/routing/integrations/next-js) y [Remix](/core/docs/routing/integrations/remix). En los siguientes pasos del tutorial verás contenido relacionado con la opción de routing que selecciones. Puedes cambiar esa selección en cualquier momento y consultar el material equivalente para otras librerías durante todo el tutorial.

Elige la librería de routing con la que quieres continuar:

<TutorialParameterDropdown parameter="routerSelection" label="Routing" className="w-min pb-4" />

En las siguientes unidades del tutorial también seleccionarás una integración de UI para Refine y verás cómo se construyen estas integraciones y en qué situaciones resultan útiles. Aunque Refine ofrece soporte oficial para Ant Design, Material UI, Mantine y Chakra UI, el tutorial está preparado para las dos bibliotecas más utilizadas: [Ant Design](/core/docs/ui-integrations/ant-design/introduction) y [Material UI](/core/docs/ui-integrations/material-ui/introduction).

Elige el framework UI con el que quieres continuar:

<TutorialParameterDropdown parameter="uiSelection" label="UI Framework" className="w-min pb-4" />

Puedes encontrar el material equivalente para las otras bibliotecas UI dentro de la [documentación](/core/docs/guides-concepts/ui-libraries).

## Contenido del tutorial

A continuación encontrarás todas las secciones del tutorial organizadas por tema:

### Fundamentos

- [Tu primera aplicación con Refine](/core/tutorial/essentials/setup/)
- [Obtener un registro](/core/tutorial/essentials/data-fetching/fetching-data/)
- [Actualizar un registro](/core/tutorial/essentials/data-fetching/updating-data/)
- [Listar registros](/core/tutorial/essentials/data-fetching/listing-data/)
- [Formularios](/core/tutorial/essentials/forms/)
- [Tablas](/core/tutorial/essentials/tables/)

### Autenticación

- [Introducción](/core/tutorial/authentication/intro/)
- [Proteger contenido](/core/tutorial/authentication/protecting-content/)
- [Iniciar y cerrar sesión](/core/tutorial/authentication/logging-in-out/)
- [Usar la identidad del usuario](/core/tutorial/authentication/user-identity/)
- [Integración del data provider](/core/tutorial/authentication/data-provider-integration/)

### Routing con React Router

- [Introducción](/core/tutorial/routing/intro/react-router/)
- [Autenticación](/core/tutorial/routing/authentication/react-router/)
- [Definir resources](/core/tutorial/routing/resource-definition/react-router/)
- [Navegación](/core/tutorial/routing/navigation/react-router/)
- [Inferir parámetros](/core/tutorial/routing/inferring-parameters/react-router/)
- [Redirecciones](/core/tutorial/routing/redirects/react-router/)
- [Sincronizar estado con la ubicación](/core/tutorial/routing/syncing-state/react-router/)

### Bibliotecas UI con Ant Design

- [Introducción](/core/tutorial/ui-libraries/intro/ant-design/react-router/)
- [Uso de layouts](/core/tutorial/ui-libraries/layout/ant-design/react-router/)
- [Refactorización](/core/tutorial/ui-libraries/refactoring/ant-design/react-router/)
- [Componentes CRUD](/core/tutorial/ui-libraries/crud-components/ant-design/react-router/)
- [Notificaciones](/core/tutorial/ui-libraries/notifications/ant-design/react-router/)
- [Autenticación](/core/tutorial/ui-libraries/authentication/ant-design/react-router/)

### Bibliotecas UI con Material UI

- [Introducción](/core/tutorial/ui-libraries/intro/material-ui/react-router/)
- [Uso de layouts](/core/tutorial/ui-libraries/layout/material-ui/react-router/)
- [Refactorización](/core/tutorial/ui-libraries/refactoring/material-ui/react-router/)
- [Componentes CRUD](/core/tutorial/ui-libraries/crud-components/material-ui/react-router/)
- [Notificaciones](/core/tutorial/ui-libraries/notifications/material-ui/react-router/)
- [Autenticación](/core/tutorial/ui-libraries/authentication/material-ui/react-router/)

### Próximos pasos con Ant Design

- [Introducción](/core/tutorial/next-steps/intro/ant-design/)
- [Uso de Inferencer](/core/tutorial/next-steps/inferencer/react-router/ant-design/)
- [Uso de la CLI](/core/tutorial/next-steps/cli/react-router/ant-design/)
- [Uso de Devtools](/core/tutorial/next-steps/devtools/react-router/ant-design/)
- [Resumen](/core/tutorial/next-steps/summary/react-router/ant-design/)

### Próximos pasos con Material UI

- [Introducción](/core/tutorial/next-steps/intro/material-ui/)
- [Uso de Inferencer](/core/tutorial/next-steps/inferencer/react-router/material-ui/)
- [Uso de la CLI](/core/tutorial/next-steps/cli/react-router/material-ui/)
- [Uso de Devtools](/core/tutorial/next-steps/devtools/react-router/material-ui/)
- [Resumen](/core/tutorial/next-steps/summary/react-router/material-ui/)

</Sandpack>
