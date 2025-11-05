# Diagrama de Paquetes: Frontend Nexa

[← Volver a Paquetes Front / Back](../DAS.md#paquetes-front--back)

## Índice
1. [Descripción General](#descripción-general)
2. [Diagrama](#diagrama)
3. [Estructura de Paquetes](#estructura-de-paquetes)
4. [Dependencias](#dependencias)

## Descripción General
Este documento describe la estructura de paquetes del frontend de Nexa, basada en una arquitectura moderna de Nuxt.js/Vue.js.

## Diagrama
![Diagrama de Paquetes Frontend](../diagramas/paquete_front.png)

## Estructura de Paquetes
Descripción: Diagrama que muestra la distribución de carpetas orientada a una estructura estándar de aplicación frontend (basada en Nuxt.js o Vue.js) y las dependencias o flujos entre ellas.

| Paquete | Paquete padre | Descripción | Usa/Importa |
| :--- | :--- | :--- | :--- |
| **nexa** | — | Paquete raíz que agrupa toda la estructura de la aplicación frontend nexa. | |
| **src** | nexa | Carpeta principal que contiene el código fuente de la aplicación. | |
| **assets** | src | Carpeta que contiene activos estáticos no compilados, como imágenes, fuentes, estilos Sass o Less, que se procesan durante la build. | |
| **components** | src | Carpeta que agrupa componentes Vue reutilizables, auto-importados en la aplicación para construir interfaces. | assets |
| **composables** | src | Carpeta que agrupa funciones composables (usando Composition API), auto-importadas para lógica reutilizable como hooks o utilidades. | |
| **views** | src | Carpeta que agrupa las vistas o páginas principales de la aplicación, definiendo las rutas y el contenido principal (equivalente a 'pages' en Nuxt). | components, composables, services |
| **services** | src | Carpeta que agrupa servicios para lógica de negocio externa, como llamadas a API, manejo de datos o integraciones con backends. | composables |