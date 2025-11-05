[🔙 Volver al README](./README.md)

# Componentes Desarrollados

| Componente | ¿Componente de Pago? | Tipo | Fabricante | Producto | Versión | Descripción | Justificación |
|------------|----------------------|------|------------|----------|---------|-------------|---------------|
| Back End Nexa | NO | Lenguaje de Desarrollo | Microsoft | TypeScript | 5.9.3 | Lenguaje moderno y tipado que mejora la calidad del código y facilita la detección de errores. Combina la flexibilidad de JavaScript con herramientas que permiten desarrollar proyectos grandes de forma más segura y mantenible. | Es la mejor opción para Nexa porque permite un desarrollo ágil, limpio y consistente entre el frontend y el backend. Además, se integra de forma nativa con los servicios cloud utilizados por la plataforma, reduciendo complejidad y costos. |
| Back End Nexa | NO | Framework de desarrollo | The NestJS Core Team (Mantenido por Kamil Myśliwiec y la comunidad de OpenJS Foundation) | NestJS | 11.1.6. | Framework robusto que ofrece una arquitectura modular, inyección de dependencias y un diseño basado en buenas prácticas como SOLID. Facilita la creación de APIs escalables, seguras y fáciles de mantener, inspirado en la estructura de Spring Boot. | Es la mejor opción para Nexa porque ofrece una arquitectura modular y escalable que facilita mantener un backend limpio, seguro y de alto rendimiento. A diferencia de frameworks más pesados como Spring Boot, NestJS aprovecha la eficiencia de Node.js y se adapta perfectamente a entornos serverless, optimizando costos y consumo de recursos. Además, su compatibilidad con TypeScript y su ecosistema moderno permiten desarrollar APIs robustas y fácilmente integrables con los servicios cloud de Nexa, como Firebase y Google Cloud. |
| Front End Nexa | NO | Lenguaje de Desarrollo | Microsoft | TypeScript | 5.9.3 | Lenguaje moderno que agrega tipado y herramientas avanzadas a JavaScript, permitiendo un código más seguro, mantenible y escalable en el frontend. | Es la mejor opción para Nexa porque mejora la calidad del código, reduce errores en tiempo de desarrollo y permite crear interfaces más estables y predecibles al trabajar junto con Nuxt.js. |
| Front End Nexa | NO | Framework de desarrollo | NuxtLabs | Spring Framework | 4.x (La más reciente y estable) | Framework moderno basado en Vue que permite crear aplicaciones web muy rápidas, reactivas y optimizadas para buscadores. Usa renderizado en servidor para mejorar el SEO, organiza automáticamente las rutas de la app y se integra de forma nativa con TypeScript para un desarrollo más seguro y ordenado. | Es la mejor opción para Nexa porque combina excelente rendimiento, alta reactividad y posicionamiento SEO gracias a su renderizado en servidor (SSR). Nuxt.js, como framework full-stack basado en Vue.js, ofrece una interfaz extremadamente dinámica y sensible a las interacciones del usuario. Además, integra de forma nativa el módulo @nuxt/image, que optimiza automáticamente las imágenes (WebP/AVIF), aplica lazy loading y adapta su tamaño a cada dispositivo. Esta combinación mejora la velocidad de carga, reduce el consumo de recursos y ofrece una experiencia visual fluida y moderna, ideal para una plataforma SaaS con catálogos altamente visuales como Nexa. |

## Backend Nexa

### Stack Tecnológico
- **Lenguaje**: TypeScript 5.9.3
- **Framework**: NestJS 11.1.6
- **Runtime**: Node.js

### Justificación
TypeScript es la mejor opción para Nexa porque permite un desarrollo ágil, limpio y consistente entre el frontend y el backend. Además, se integra de forma nativa con los servicios cloud utilizados por la plataforma, reduciendo complejidad y costos.

NestJS es la mejor opción porque ofrece una arquitectura modular y escalable que facilita mantener un backend limpio, seguro y de alto rendimiento. A diferencia de frameworks más pesados como Spring Boot, NestJS aprovecha la eficiencia de Node.js y se adapta perfectamente a entornos serverless, optimizando costos y consumo de recursos.

### Características Principales
- Arquitectura modular
- Inyección de dependencias
- Middleware system
- WebSocket support
- OpenAPI (Swagger)
- Validación incorporada
- Testing utilities

## Frontend Nexa

### Stack Tecnológico
- **Lenguaje**: TypeScript 5.9.3
- **Framework**: Nuxt.js 4.x
- **Runtime**: Node.js

### Justificación
TypeScript mejora la calidad del código, reduce errores en tiempo de desarrollo y permite crear interfaces más estables y predecibles al trabajar junto con Nuxt.js.

Nuxt.js es la mejor opción porque combina excelente rendimiento, alta reactividad y posicionamiento SEO gracias a su renderizado en servidor (SSR). Como framework full-stack basado en Vue.js, ofrece una interfaz extremadamente dinámica y sensible a las interacciones del usuario.

### Características Principales
- SSR/SSG híbrido
- Auto-import
- SEO optimization
- Image optimization
- TypeScript support
- Hot module replacement
