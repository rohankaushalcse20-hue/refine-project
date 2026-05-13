---
title: Introducción
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Ahora ya aprendimos los fundamentos de data fetching y manipulación de datos en Refine. En esta unidad aprenderemos a agregar autenticación a nuestra aplicación y los conceptos esenciales de autenticación en Refine.

Refine proporciona una interfaz de autenticación fácil de gestionar que puede usarse con cualquier proveedor de autenticación con muy poco esfuerzo.

Esta unidad cubrirá los siguientes temas:

- Aprender la interfaz [`AuthProvider`](/core/docs/authentication/auth-provider) creando un proveedor de autenticación,
- Usar hooks y componentes de auth como los hooks [`useLogin`](/core/docs/authentication/hooks/use-login), [`useIsAuthenticated`](/core/docs/authentication/hooks/use-is-authenticated) y el componente [`<Authenticated />`](/core/docs/authentication/components/authenticated).
- Gestionar la autenticación en data providers y manejar errores de autenticación.

Esta unidad será agnóstica al router y al framework UI. Las partes de autenticación relacionadas con el router y el framework UI se cubrirán en las próximas unidades.

</Sandpack>
