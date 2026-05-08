---
title: "Guía de telemetría | Buenas prácticas en Refine v5"
display_title: "Telemetría"
description: "Entiende qué datos recopila Refine, por qué los recopila y cómo desactivar la telemetría en la app y en la CLI."
sidebar_label: "Telemetría"
---

import Tabs from "@theme/Tabs";
import TabItem from "@theme/TabItem";

# Telemetría

## Resumen

**Refine** implementa un módulo de telemetría **simple** y **transparente** para recopilar estadísticas de uso definidas dentro de un alcance **muy limitado**.

El seguimiento es totalmente **seguro** y cada persona puede seguir siendo **anónima** sin aportar información personal identificable.

Al configurar un proyecto nuevo, existe un paso adicional y opcional en el que pedimos la **dirección de correo electrónico** de la persona desarrolladora.

Si se proporciona, esta información de contacto se recopila y se vincula al proyecto. Se usa ocasionalmente para contactar a miembros de la comunidad; nunca la compartimos con terceros ni la utilizamos para enviar spam.

El sistema de telemetría **no usa cookies**. La participación es opcional y cualquier usuario puede **desactivarla** con facilidad.

## ¿Por qué la necesitamos?

Intentamos responder a la pregunta de **cuántas personas usan activamente el framework Refine**. Esta información es importante para proyectos open source como Refine porque ayuda a entender mejor a la comunidad y a medir su crecimiento.

## ¿Cómo recopilamos datos?

<Tabs>
    <TabItem value="refine-core" label="Refine core" default>

La recopilación ocurre cuando una aplicación Refine se carga en el navegador del usuario. Durante la inicialización de la aplicación, se envía una única solicitud HTTP a `"https://telemetry.refine.dev"`. El cuerpo de la solicitud se codifica con Base64 para que los servidores de Refine puedan decodificarlo.

No se envían solicitudes adicionales durante esa sesión, ya que NO recopilamos información de comportamiento como _page views_, _button clicks_, etc.

<h2>¿Qué se recopila?</h2>

La llamada HTTP envía una carga JSON con los siguientes atributos específicos de la aplicación:

| Valor         | Tipo        | Descripción                                                                                                                           |
| ------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| providers     | `boolean[]` | Lista de providers usados en el proyecto (`auth`, `data`, `router`, `live`, `notification`, `auditLog`, `i18n` o `accessControl`) |
| version       | `string`    | Versión del paquete de Refine.                                                                                                        |
| resourceCount | `number`    | Número total de resources.                                                                                                            |

Además, se extrae y recopila la siguiente información desde el encabezado HTTP:

| Valor        | Descripción                                                   |
| ------------ | ------------------------------------------------------------- |
| IP Address   | Dirección IP de la máquina desde la que llega la petición.    |
| Hostname     | Nombre del host de la máquina desde la que llega la petición. |
| Browser      | Navegador y versión del navegador.                            |
| OS           | Sistema operativo y versión del sistema operativo.            |

Por último, recopilamos la información de contacto, **si se proporciona** al crear el proyecto.

| Valor         | Descripción                                             |
| ------------- | ------------------------------------------------------- |
| Email Address | Dirección de correo de la persona desarrolladora. [**OPTIONAL**] |

:::note

refine.new es la alternativa en la nube a la CLI para crear proyectos de Refine.
Requiere iniciar sesión con una cuenta de GitHub y recopila un conjunto limitado de datos públicos del perfil con fines analíticos. Los datos recopilados también pueden vincularse automáticamente al proyecto creado.

Los proyectos creados con refine.new también pueden desactivar la telemetría simplemente añadiendo el prop `disableTelemetry` dentro de `options` en el componente `<Refine>`.

:::

<h2>¿Cómo se desactiva?</h2>

Puedes desactivar la telemetría añadiendo el prop `disableTelemetry` dentro de `options` en el componente `<Refine>`.

  </TabItem>

<TabItem value="refine-cli" label="Refine CLI">

Después de ejecutar un comando con la CLI de `Refine`, se envía una única solicitud HTTP a `"https://telemetry.refine.dev/cli"`.

<h2>¿Qué se recopila?</h2>

| Valor            | Tipo                                          | Descripción                                                        |
| ---------------- | --------------------------------------------- | ------------------------------------------------------------------ |
| nodeEnv          | `string`                                      | Especifica el entorno en el que se está ejecutando la aplicación. |
| nodeVersion      | `string`                                      | Versión instalada de Node.js.                                      |
| os               | `string`                                      | Nombre del sistema operativo.                                      |
| osVersion        | `string`                                      | Versión del sistema operativo.                                     |
| command          | `string`                                      | Nombre del script ejecutado.                                       |
| packages         | `{ "name": "string", "version": "string" }[]` | Paquetes `Refine` instalados.                                      |
| projectFramework | `string`                                      | Framework de `react` instalado.                                    |

Además, se extrae y recopila la siguiente información desde el encabezado HTTP:

| Valor      | Descripción                                                |
| ---------- | ---------------------------------------------------------- |
| IP Address | Dirección IP de la máquina desde la que llega la petición. |

:::note

refine.new es la alternativa en la nube a la CLI para crear proyectos de Refine.
Requiere iniciar sesión con una cuenta de GitHub y recopila un conjunto limitado de datos públicos del perfil con fines analíticos. Los datos recopilados también pueden vincularse automáticamente al proyecto creado.

Los proyectos creados con refine.new también pueden desactivar la telemetría simplemente añadiendo el prop `disableTelemetry` dentro de `options` en el componente `<Refine>`.

:::

<h2>¿Cómo se desactiva?</h2>

Puedes desactivar la telemetría añadiendo `REFINE_NO_TELEMETRY=true` a las variables de entorno.

</TabItem>
</Tabs>
