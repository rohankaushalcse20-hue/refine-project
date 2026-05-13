---
title: Tu primera app con Refine
---

import { Sandpack } from "./sandpack.tsx";

<Sandpack>

Crear una nueva app de Refine es muy sencillo y solo requiere unos pocos pasos para generar una aplicación completamente funcional. Para este tutorial, no usaremos `create-refine-app` con todo su potencial. En su lugar, crearemos una app vacía, instalaremos las dependencias necesarias y configuraremos la aplicación manualmente.

<Tabs wrapContent={false}>

<TabItem value="quick" label="Configuración rápida">

Para seguir este tutorial, puedes usar las plantillas iniciales que ofrece `create-refine-app`. El siguiente comando creará un proyecto vacío con los paquetes `@refinedev/core` y `@refinedev/cli`, con todo lo necesario para comenzar el tutorial.

```sh
npm create refine-app@latest -- --example starter-vite
```

</TabItem>

<TabItem value="manual" label="Configuración manual">

Necesitaremos crear nuestra app con las plantillas adecuadas. Después instalaremos las dependencias de Refine y configuraremos la aplicación.

```sh
npm create vite@latest my-refine-app -- --template react-ts
```

Para obtener más información sobre Vite y la creación de proyectos, puedes visitar la [documentación de Vite](https://vitejs.dev/guide/#scaffolding-your-first-vite-project).

Después de crear el proyecto, necesitaremos instalar las dependencias de Refine.

```sh
npm install @refinedev/core @refinedev/cli
```

Estamos instalando `@refinedev/core`, que proporciona todas las funcionalidades principales de Refine, y `@refinedev/cli`, que aunque es opcional, aporta muchas funciones útiles para el proceso de desarrollo. Para obtener más información sobre `@refinedev/cli`, puedes visitar [su documentación](/core/docs/packages/cli).

### Configurar los scripts

Reemplazaremos nuestros scripts `dev`, `build` y `serve` por los siguientes:

```json
{
  "scripts": {
    "dev": "refine dev",
    "build": "refine build",
    "serve": "refine serve"
  }
}
```

Aunque los comandos ejecutores de `refine` usarán los mismos comandos que proporciona el bundler, también aportarán funciones útiles como comprobaciones de versión de dependencias y anuncios del equipo de Refine.

### Configurar la app

Necesitaremos montar el componente `<Refine />` en nuestra app. Lo montaremos en la raíz de la aplicación.

```tsx title="src/App.tsx"
import { Refine, WelcomePage } from "@refinedev/core";

function App() {
  return (
    <Refine>
      <WelcomePage />
    </Refine>
  );
}

export default App;
```

Aquí no estamos haciendo nada especial. Solo estamos montando el componente `<Refine />` en la app. El componente `<Refine />` es el componente central de Refine y proporciona todo el contexto y la lógica necesarios para que la aplicación funcione.

El componente `<WelcomePage />` lo proporciona `@refinedev/core` y es una página sencilla que te da la bienvenida a Refine. Puedes eliminarlo si lo deseas.

Esto será suficiente para que nuestra app funcione. Ahora podemos iniciarla con el siguiente comando:

```sh
npm run dev
```

Cuando abras el navegador y vayas a localhost, deberías ver la página de la derecha. Si todo funciona como se espera, continúa con la siguiente sección.

</TabItem>

</Tabs>

:::tip Generación de apps a medida

De forma predeterminada, `create-refine-app` te guía por varios pasos para crear una app adaptada a tus necesidades, desde data providers hasta autenticación, bibliotecas UI y más. Puedes leer más sobre esto en la sección de [quickstart](/core/docs/getting-started/quickstart).

:::

</Sandpack>
