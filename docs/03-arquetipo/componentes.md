[🔙 Volver al README](./README.md)

# Detalle de Componentes

Para Nexa, la alternativa seleccionada se basa en componentes como WAF, API Gateway, etc., porque equilibran seguridad, escalabilidad y costos bajos. Se elige sobre otras (ej. AWS full) por conveniencia despues de analizar cada posible tecnologia, integración con Firebase/Stripe y foco en SaaS.

## Diagrama del Arquetipo
![Arquetipo de Referencia](../../diagramas/arqueotipo.png)

## Diagramas Relacionados
- [Diagrama de Componentes Backend](../../diagramas/componentes_backend.png)
- [Diagrama de Componentes Frontend](../../diagramas/componentes_front.png)
- [Diagrama de Arquitectura del Sistema](../../diagramas/arquitectura.png)

| Componente | Tipo componente | Descripción | Justificación | ¿Es un bloque de construcción? | Tipo Componente Construcción |
|------------|-----------------|-------------|---------------|--------------------------------|------------------------------|
| WAF | Componente adoptado | Ver descripción | Para Nexa, el WAF es un componente imprescindible porque actúa como un escudo que protege la aplicación frente a amenazas externas. Su función es revisar las solicitudes que llegan al sistema y bloquear aquellas que puedan ser maliciosas. Gracias a esto, evita ataques comunes que podrían dañar o alterar el funcionamiento de la plataforma, ayudando a mantenerla segura, estable y confiable para todos sus usuarios. | SI | Genérico |
| API GATEWAY | Componente adoptado | Ver descripción | Para Nexa, el API Gateway es un componente fundamental porque funciona como la puerta principal por donde pasan todas las solicitudes hacia la aplicación. Su trabajo consiste en recibir las peticiones de los usuarios y enviarlas al servicio correcto dentro del sistema. Este componente es muy importante para mantener la aplicación rápida y estable, ya que se encarga de distribuir el tráfico de forma equilibrada. Gracias a él, Nexa puede atender a muchos usuarios al mismo tiempo sin perder rendimiento ni disponibilidad. | SI | Genérico |
| IDENTITY MANAGEMENT | Componente adoptado | Ver descripción | Para Nexa, el componente de Identity Management es esencial porque permite que solo los usuarios autorizados puedan acceder a la plataforma. Este servicio se encarga de manejar los inicios de sesión, verificar que las credenciales sean correctas y emitir los permisos necesarios para cada sesión. Gracias a él, se protege la privacidad de los usuarios y se mantiene un control seguro de quién entra y qué acciones realiza dentro del sistema. | SI | Genérico |
| PAYMENTS | Componente adoptado | Ver descripción | Para Nexa, el servicio de pagos es un componente imprescindible porque hace posible que las suscripciones y transacciones se realicen de manera segura y confiable. Este servicio se encarga de procesar los pagos, proteger los datos sensibles de los usuarios y mantener disponibles los diferentes medios de cobro. Gracias a él, los emprendedores pueden activar y mantener sus tiendas sin complicaciones. | SI | Genérico |
| NOTIFICATIONS | Componente adoptado | Ver descripción | Para Nexa, el servicio de notificaciones es un componente esencial porque permite mantener una comunicación rápida y efectiva con los usuarios. Gracias a este servicio, la plataforma puede informar de manera oportuna sobre transacciones, actualizaciones o cambios importantes. Esto mejora la experiencia de los usuarios y garantiza que siempre estén al tanto de lo que ocurre dentro de la aplicación. | SI | Genérico |
| CACHE | Componente adoptado | Ver descripción | Para Nexa, el componente de caché es fundamental porque ayuda a que la plataforma funcione de forma rápida y fluida. Su función es guardar temporalmente la información que se usa con frecuencia, evitando que el sistema tenga que buscarla en la base de datos cada vez. Esto hace que las respuestas sean mucho más rápidas, reduce el consumo de recursos y ofrece a los usuarios una experiencia más ágil y confiable. | SI | Genérico |
| KEY VAULT | Componente adoptado | Ver descripción | Para Nexa, el Key Vault es un componente esencial porque funciona como una caja fuerte digital donde se guardan de forma segura las claves, certificados y datos confidenciales que usa la plataforma. Gracias a este servicio, se protegen las credenciales más sensibles y se evita que información importante pueda quedar expuesta o ser accedida por personas no autorizadas, fortaleciendo así la seguridad general del sistema. | SI | Genérico |
| STORAGE | Componente adoptado | Ver descripción | Para Nexa, el componente de almacenamiento es fundamental para conservar los recursos multimedia y documentos asociados al catálogo digital de cada usuario. Este componente asegura la disponibilidad, durabilidad y acceso eficiente a los archivos. | SI | Genérico |
| AUTHENTICATION | Componente adoptado | Ver descripción | Para Nexa, el servicio de autenticación es un componente indispensable que valida las credenciales y tokens emitidos por el sistema de identidad, garantizando que cada solicitud provenga de un usuario autorizado. Este componente protege la integridad de las operaciones y asegura que solo usuarios legítimos puedan acceder a funcionalidades del sistema. |  |  |
| DATABASE | Componente adoptado | Ver descripción | Para Nexa, la base de datos es un componente imprescindible que almacena de manera organizada y segura toda la información importante del sistema, como los usuarios, catálogos, productos y transacciones. Gracias a ella, los datos se mantienen siempre disponibles, coherentes y confiables, garantizando el correcto funcionamiento de la plataforma. | SI | Genérico |
| MONITORING PLATFORM | Componente adoptado | Ver descripción | Para Nexa, la plataforma de monitoreo es un componente indispensable porque permite revisar en todo momento el funcionamiento de la aplicación. A través de registros, métricas y trazas, se pueden detectar errores, cuellos de botella o posibles vulnerabilidades antes de que afecten a los usuarios. Esto garantiza que el servicio esté disponible las 24 horas del día y que la plataforma funcione de manera estable y confiable. | SI | Genérico |
| PARAM CATALOG | Componente adoptado | Ver descripción | Para Nexa, el módulo Parameters Catalog es clave para ajustar reglas de negocio sin tocar el código. Permite configurar límites, formatos y funcionalidades según tienda, suscripción o rol, manteniendo la escalabilidad y trazabilidad. Sin este catálogo, cada cambio requeriría intervención técnica, afectando la agilidad y la experiencia del usuario. | SI | Genérico |
| BACKEND | Desarrollo propio |  | Para Nexa, el backend es un componente esencial porque allí se ejecuta toda la lógica principal de la plataforma, como crear pedidos o gestionar productos. Este componente se encarga de procesar las solicitudes que llegan desde el frontend y otros servicios, asegurando que todo funcione de forma segura, rápida y confiable. Además, garantiza la disponibilidad y la integridad de los datos, lo que permite que Nexa opere de manera estable en todo momento. | SI | Core |
| FRONTEND | Desarrollo propio |  | Para Nexa, el frontend es un componente imprescindible porque es lo que los usuarios ven al interactuar con la plataforma. Su diseño visual y facilidad de uso son clave para atraer y retener a los usuarios, ya que ofrece una experiencia moderna, fluida y agradable. Gracias a este componente, Nexa logra transmitir confianza y profesionalismo desde el primer contacto con el emprendedor. | SI | Core |
| CLOUD APPLICATION PLATFORM | Componente adoptado | Ver descripción | Para Nexa, una Cloud Application Platform es un componente esencial porque permite construir y ejecutar el backend de forma segura, escalable y confiable. Esta plataforma ofrece toda la infraestructura necesaria sin que sea necesario administrar servidores manualmente. Gracias a ello, Nexa puede mantener una arquitectura moderna basada en la nube, que se adapta fácilmente a la demanda del negocio y garantiza que los servicios estén siempre disponibles y funcionando sin interrupciones. | SI | Genérico |
| CLOUD APPLICATION PLATFORM | Componente adoptado | Ver descripción | Dentro de la arquitectura de Nexa, una Cloud Application Platform cumple un papel clave en cómo se entrega y actualiza el frontend. Gracias a su infraestructura sin servidores y a su red de distribución de contenido (CDN), permite que la aplicación esté disponible en todo el mundo y que las páginas se carguen rápido y sin interrupciones. Además, su capacidad para escalar automáticamente garantiza que el frontend siempre funcione de forma segura, confiable y alineada con los principios de una arquitectura moderna en la nube. | SI | Genérico |

## Componentes de Infraestructura

### WAF
- **Tipo**: Componente adoptado
- **Descripción**: Firewall de aplicación web
- **Justificación**: Protección esencial contra amenazas web
- **Bloque de Construcción**: Genérico

### API Gateway
- **Tipo**: Componente adoptado
- **Descripción**: Gestión y control de APIs
- **Justificación**: Control centralizado de tráfico
- **Bloque de Construcción**: Genérico

## Componentes de Seguridad

### Identity Management
- **Tipo**: Componente adoptado
- **Descripción**: Gestión de identidades y accesos
- **Justificación**: Control de acceso seguro
- **Bloque de Construcción**: Genérico

### Key Vault
- **Tipo**: Componente adoptado
- **Descripción**: Gestión segura de secretos
- **Justificación**: Protección de credenciales
- **Bloque de Construcción**: Genérico

## Componentes de Negocio

### Payments
- **Tipo**: Componente adoptado
- **Descripción**: Procesamiento de pagos
- **Justificación**: Gestión segura de transacciones
- **Bloque de Construcción**: Genérico

### Backend
- **Tipo**: Desarrollo propio
- **Descripción**: Lógica de negocio
- **Justificación**: Core funcional del sistema
- **Bloque de Construcción**: Core

### Frontend
- **Tipo**: Desarrollo propio
- **Descripción**: Interfaz de usuario
- **Justificación**: Experiencia de usuario
- **Bloque de Construcción**: Core

## Componentes de Datos

### Cache
- **Tipo**: Componente adoptado
- **Descripción**: Caché de datos
- **Justificación**: Mejora de rendimiento
- **Bloque de Construcción**: Genérico

### Storage
- **Tipo**: Componente adoptado
- **Descripción**: Almacenamiento de archivos
- **Justificación**: Gestión de recursos
- **Bloque de Construcción**: Genérico

### Database
- **Tipo**: Componente adoptado
- **Descripción**: Base de datos principal
- **Justificación**: Persistencia de datos
- **Bloque de Construcción**: Genérico

## Componentes de Operación

### Monitoring Platform
- **Tipo**: Componente adoptado
- **Descripción**: Monitoreo del sistema
- **Justificación**: Control operacional
- **Bloque de Construcción**: Genérico

### Parameters Catalog
- **Tipo**: Componente adoptado
- **Descripción**: Gestión de configuración
- **Justificación**: Flexibilidad operativa
- **Bloque de Construcción**: Genérico

### Cloud Application Platform
- **Tipo**: Componente adoptado
- **Descripción**: Infraestructura cloud
- **Justificación**: Base operativa escalable
- **Bloque de Construcción**: Genérico