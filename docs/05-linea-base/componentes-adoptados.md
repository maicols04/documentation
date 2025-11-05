[🔙 Volver al README](./README.md)

# Componentes Adoptados

| Componente | ¿Componente de Pago? | Fabricante | Producto | Versión | Protocolo de comunicación | Justificación | Tipo Bloque Construcción |
|------------|----------------------|------------|----------|---------|---------------------------|---------------|--------------------------|
| WAF | SI | Cloudflare, Inc. | Cloudflare WAF | Latest | https | Cloudflare WAF es la mejor opción para Nexa porque proporciona protección efectiva y escalable contra ataques web comunes, manteniendo la seguridad de la plataforma sin complicaciones. Su eficiencia, facilidad de uso y escalabilidad lo convierten en la alternativa ideal para un SaaS que necesita proteger su aplicación web de manera confiable, sin sobrecostos ni complejidad técnica. | Genérico |
| API GATEWAY | SI | Google Cloud | Google Cloud API Gateway | Latest | https | Para Nexa, Google Cloud API Gateway es la mejor opción porque combina seguridad, escalabilidad y facilidad de uso. Al ser un servicio totalmente gestionado, garantiza alta disponibilidad y capacidad para escalar automáticamente, distribuyendo el tráfico entre las instancias del backend y asegurando un funcionamiento estable incluso en picos de uso. Además, reduce la carga de mantenimiento para el equipo, que puede concentrarse en mejorar la experiencia de los usuarios. Su modelo de costos flexible, basado en el uso real, lo hace ideal para una startup SaaS como Nexa, asegurando eficiencia y confiabilidad desde el principio. | Genérico |
| IDENTITY MANAGEMENT | SI | Google Cloud | Firebase Auth | Latest | https | La mejor opción para el Identity Management de NEXA es Firebase Authentication. Gestiona de forma segura todo el ciclo de vida del usuario (registro, inicio de sesión, restablecimiento de contraseña y autenticación multifactor (MFA)), simplificando la implementación y reduciendo la complejidad del desarrollo. Su modelo pago por uso con nivel gratuito generoso lo hace accesible y escalable para startups. | Genérico |
| PAYMENTS | SI | Stripe Inc. | Stripe Billing | Latest | https | Stripe es la mejor opción para Nexa porque combina potencia, seguridad y una integración sencilla en un solo servicio. A diferencia de otras pasarelas, Stripe está pensado específicamente para modelos SaaS con pagos recurrentes, permitiendo gestionar planes flexibles, facturación automática y trazabilidad completa. Su infraestructura global y cumplimiento con PCI DSS garantizan transacciones seguras y confiables. En términos de costo-beneficio, escalabilidad y soporte técnico, supera a alternativas como PayPal o MercadoPago, consolidándose como la opción más estratégica y sostenible para el crecimiento de Nexa. | Genérico |
| NOTIFICATIONS | SI | Sinch | Mailgun send | Latest | https | Mailgun representa la mejor opción para Nexa porque, aunque el envío de emails no es el núcleo de la plataforma, permite que los clientes reciban solo las notificaciones necesarias para mantenerse actualizados de manera confiable y segura. Ofrece automatización y trazabilidad completas de los correos transaccionales, asegurando que confirmaciones, recordatorios y alertas lleguen correctamente. En comparación con otras soluciones, Mailgun ofrece un balance óptimo entre facilidad de uso, seguridad, escalabilidad y soporte, siendo la opción más eficiente y estratégica para cubrir las necesidades de comunicación de Nexa. | Genérico |
| CACHE | SI | Redis Ltd | Redis | Latest | tcp/ip | Redis es la mejor opción para Nexa porque permite guardar información importante de forma rápida y confiable, como las sesiones de los usuarios y los carritos de compras. Esto hace que la plataforma sea ágil y que los datos se actualicen en tiempo real sin sobrecargar la base de datos principal. Además, es fácil de integrar con el backend de Nexa. En resumen, Redis asegura que Nexa funcione rápido, estable y de manera eficiente para los usuarios. | Genérico |
| KEY VAULT | SI | Google Cloud | Google Cloud Secret Manager | Latest | https | Google Cloud Secret Manager es la mejor opción como Key Vault para Nexa porque permite almacenar y gestionar de forma segura todas las credenciales, claves de API y secretos de la plataforma desde un único lugar. Su control de acceso IAM garantiza que solo las instancias autorizadas del backend puedan acceder a secretos críticos, evitando que queden expuestos en el código o repositorios. Además, al ser un servicio gestionado y escalable, ofrece funciones de seguridad de nivel empresarial como versionado, rotación automática de secretos y auditoría de accesos, esenciales para la confiabilidad y el cumplimiento normativo. Su modelo de pago por uso asegura que los costos sean mínimos y predecibles, adaptándose perfectamente a las necesidades de Nexa como plataforma SaaS en crecimiento. | Genérico |
| STORAGE | SI | Google Cloud | Firebase Storage | Latest | https | Firebase Storage es la opción ideal para Nexa porque proporciona un almacenamiento seguro, escalable y confiable para todos los archivos de la plataforma. Permite guardar grandes volúmenes de datos sin preocuparse por la infraestructura ni la gestión de servidores. Gracias a su rendimiento rápido y a la escalabilidad automática, Nexa puede manejar el crecimiento de su catálogo y la demanda de los clientes de manera eficiente y segura, asegurando que los archivos siempre estén disponibles. | Genérico |
| AUTHENTICATION | SI | Google Cloud | Firebase Auth | Latest | https | La mejor opción para Nexa porque permite manejar de manera segura y eficiente el registro, inicio de sesión y gestión de usuarios. Soporta múltiples métodos de autenticación y, al estar gestionado por Google, elimina preocupaciones sobre seguridad, mantenimiento y escalabilidad, garantizando accesos confiables y sin interrupciones. | Genérico |
| DATABASE | SI | Google Cloud | Firebase Firestore | Latest | https | Firestore es la mejor opción para Nexa porque ofrece una base de datos en la nube, segura, escalable y confiable, ideal para almacenar productos, catálogos, pedidos y configuraciones de tiendas. Permite realizar consultas rápidas y flexibles, asegurando que la información siempre esté organizada y accesible. Al estar totalmente gestionada por Google, Nexa no necesita preocuparse por servidores, backups ni escalabilidad, y puede enfocarse en la funcionalidad principal de la plataforma. Firestore garantiza que la base de datos sea fiable, eficiente y lista para crecer junto con Nexa. | Genérico |
| MONITORING PLATFORM | SI | Google Cloud | Google Cloud Observability | Latest | https | Google Cloud Observability es ideal para Nexa porque ofrece monitoreo en tiempo real, alertas automáticas y registro centralizado de errores y rendimiento, todo dentro del mismo entorno de Google Cloud. Permite detectar fallas con rapidez, analizar el tráfico y asegurar que la plataforma funcione de manera estable sin depender de herramientas externas. Además, su modelo de pago por uso y su generosa capa gratuita garantizan una máxima eficiencia en costos en la fase inicial y una escalabilidad predecible y financieramente responsable a medida que la plataforma SaaS crece. | Genérico |
| PARAMETERS CATALOG | SI | Google Cloud | Firebase Remote Config | Latest | https | Firebase Remote Config es la solución óptima para el Catálogo de Parámetros de Nexa porque ofrece una gestión de configuración centralizada y dinámica, esencial para una plataforma SaaS multi-tienda. Permite al equipo de Nexa activar o desactivar funcionalidades (feature flags) o modificar límites de negocio (por ejemplo, el máximo de artículos por tienda) desde una consola central, sin necesidad de modificar ni redeplegar el código. | Genérico |
| CLOUD APPLICATION PLATFORM | SI | Render, Inc. | Render | Latest | https | Render es la mejor opción para el backend de Nexa porque combina simplicidad, eficiencia de costos y escalabilidad en un solo servicio. A diferencia de plataformas complejas como AWS o Azure, ofrece un modelo PaaS que elimina la gestión de servidores y reduce la complejidad técnica, con un pago por uso transparente que evita altos costos fijos y facturas inesperadas. Permite desplegar el backend dockerizado de manera rápida y confiable, y ofrece escalabilidad vertical y horizontal según la demanda, asegurando un rendimiento estable y eficiente a medida que Nexa crece y su base de usuarios aumenta. | Genérico |
| CLOUD APPLICATION PLATFORM | SI | Vercel, Inc. | Vercel | Latest | https | Vercel es la mejor opción para el frontend de Nexa porque ofrece una CDN global integrada optimizada específicamente para Nuxt, garantizando máximo rendimiento y SEO al servir los catálogos y páginas de las tiendas a gran velocidad en cualquier lugar del mundo. Además, minimiza los costos operativos gracias a su escalabilidad instantánea y despliegue zero-config, permitiendo a Nexa enfocarse completamente en desarrollar nuevas funcionalidades sin preocuparse por la infraestructura de hosting. | Genérico |

## Servicios de Infraestructura

### WAF (Cloudflare)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Protección efectiva contra amenazas web

### API Gateway (Google Cloud)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Gestión centralizada de APIs

## Servicios de Autenticación

### Identity Management (Firebase Auth)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Gestión segura de usuarios

### Authentication (Firebase Auth)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Validación robusta de accesos

## Servicios de Datos

### Cache (Redis)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: TCP/IP
- **Justificación**: Caché de alto rendimiento

### Storage (Firebase Storage)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Almacenamiento escalable

### Database (Firestore)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Base de datos NoSQL en tiempo real

## Servicios de Negocio

### Payments (Stripe)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Procesamiento seguro de pagos

### Notifications (Mailgun)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Envío confiable de correos

## Servicios de Operación

### Monitoring (Cloud Observability)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Monitoreo comprehensivo

### Parameters (Firebase Remote Config)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Configuración dinámica

## Plataformas de Aplicación

### Backend Platform (Render)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: PaaS simple y eficiente

### Frontend Platform (Vercel)
- **Tipo**: Componente de pago
- **Versión**: Latest
- **Protocolo**: HTTPS
- **Justificación**: Optimizado para Nuxt.js