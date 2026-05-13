---
title: Usar Devtools
---

import { Sandpack, SelectorButtonIcon } from "./sandpack.tsx";

<Sandpack>

En este paso exploraremos el potente paquete Devtools de Refine, que ofrece funciones de monitorización y actualización para inspeccionar y depurar aplicaciones Refine.

:::note

`@refinedev/devtools` está en fase beta y pronto se actualizará con todavía más funciones y mejoras.

:::

El paquete `@refinedev/devtools` está diseñado para ayudarte durante el proceso de desarrollo y se eliminará de los builds de producción. No habrá impacto de rendimiento en tu aplicación ni código sobrante en el bundle de producción.

## Instalación

La instalación del paquete es directa, pero el paquete `@refinedev/cli` también proporciona un comando para instalar y configurar el paquete Devtools. Usaremos el siguiente comando para instalar Devtools:

<Tabs>

<TabItem value="cli" label="Using CLI" default>

```sh
npm run refine devtools init
```

</TabItem>

<TabItem value="manual" label="manual">

<InstallPackagesCommand args="@refinedev/devtools" />

Después necesitaremos envolver nuestra aplicación con el componente `<DevtoolsProvider />`. El componente `<DevtoolsProvider />` debe envolver al componente `<Refine />` en el componente `App`. También importaremos el componente `<DevtoolsPanel />` para tener un acceso directo cómodo que abra Devtools en nuestra aplicación.

```tsx title="src/App.tsx"
import { Refine } from "@refinedev/core";
// highlight-next-line
import { DevtoolsProvider, DevtoolsPanel } from "@refinedev/devtools";
/* ... */

export default function App() {
    return (
        {/* highlight-start */}
        {/* You can mount the DevtoolsProvider at the top most level of the element tree */}
        <DevtoolsProvider>
        {/* highlight-end */}
            <Refine>
                {/* ... */}
            </Refine>
            {/* highlight-start */}
            {/* DevtoolsPanel component should be mounted inside the DevtoolsProvider */}
            <DevtoolsPanel />
            {/* highlight-end */}
            {/* ... */}
        {/* highlight-next-line */}
        </DevtoolsProvider>
    );
}
```

Después podremos empezar a usar Devtools en nuestra aplicación.

</TabItem>

</Tabs>

## Usar la función de monitorización

Después de instalar y configurar el paquete Devtools, aparecerá un pequeño panel devtools en la parte inferior de tu aplicación. Al hacer clic se abrirán las devtools y podrás acceder a la pantalla de monitorización haciendo clic en `"Monitor"` en la barra lateral.

Esta pantalla incluirá todas las queries y mutaciones disparadas en tu aplicación durante la sesión currentPage. Puedes ver detalles como la respuesta, el data provider objetivo, el resource objetivo, el tiempo que tardó en ejecutarse la query o mutación, y mucho más.

Puedes filtrar las queries y mutaciones por tipo, resource, estado y el componente o hook que las disparó. También puedes seleccionar en tu UI el componente por el que quieres filtrar usando el selector.

Para usar el selector, haz clic en el icono <SelectorButtonIcon /> y, cuando pases el cursor sobre un componente de tu página que haya disparado una query o una mutación, aparecerá un resaltado alrededor del componente. Al hacer clic en el componente, se filtrarán las queries y mutaciones por ese componente.

<VideoInView src="https://refine.ams3.cdn.digitaloceanspaces.com/assets/tutorial/webm/devtools-xray-3.webm" playsInline loop autoPlay muted />

## Usar la función de actualización

La función de actualización del paquete Devtools es similar al comando update de `@refinedev/cli` y te ofrece una UI cómoda para actualizar tus dependencias de Refine con un solo clic. Con el mismo panel, también puedes agregar nuevos paquetes de Refine a tu aplicación con un solo clic y aprender cómo usarlos en tu aplicación.

Consulta la pestaña `"Overview"` para ver las actualizaciones disponibles y haz clic en el botón `"Add Package"` para agregar nuevos paquetes de Refine a tu aplicación.

</Sandpack>
