[🔙 Volver al README](./README.md)

## Diagrama de Componentes para el Componente: Nexa (Frontend)

| **Componente** | **Estereotipo / Versión** | **Descripción** | **Motivación** | **Depende / Usa** | **Tipo** |
| --------------- | -------------------------- | ---------------- | ---------------- | ------------------ | -------- |
| **Nexa** | <<>dist>> nexa | Componente que representa el **frontend** de la aplicación Nexa, construido sobre un framework para interfaces de usuario reactivas y optimizadas para web. Integra lógica de presentación y consumo de servicios externos. | Artefacto final de la solución de frontend. | **nuxt.js 4**, **Node.js 22** | **Componente Propio a desarrollar** |
| **nuxt.js 4** | <<>framework/project>> nuxt.js 4 | Framework basado en **Vue.js** para el desarrollo de aplicaciones web full-stack, con soporte para **SSR (Server-Side Rendering)**, **SSG**, y características de optimización. | Acelerar el desarrollo y concentrar los esfuerzos del equipo en tareas y aspectos netamente del negocio, facilitando la creación de interfaces modernas y performantes. | **Node.js 22** | **Componente Externo (Framework/Acelerador)** |
| **Node.js 22** | <<>runtime>> Node.js 22 | Ambiente de ejecución para el código **JavaScript/TypeScript**. Permite que **Nuxt.js** y el artefacto **Nexa** puedan ser ejecutados en el servidor (para SSR/SSG) o en el proceso de compilación. | Es la plataforma base que provee el motor **V8** y el **Event Loop** necesarios para la ejecución del framework y la aplicación. | — | **Componente Externo (Runtime)** |
