[🔙 Volver al README](./README.md)

# 4. Arquitectura de Solución

La arquitectura de solución representa la implementación específica del arquetipo para Nexa, detallando los productos y tecnologías concretas seleccionadas para cada componente.

## Componentes Específicos

| Componente | Fabricante | Producto | Versión | Protocolo |
|------------|------------|----------|----------|-----------|
| WAF | Cloudflare | Cloudflare WAF | Latest | HTTPS |
| API Gateway | Google Cloud | Cloud API Gateway | Latest | HTTPS |
| Identity Management | Google Cloud | Firebase Auth | Latest | HTTPS |
| Payments | Stripe | Stripe Billing | Latest | HTTPS |
| Notifications | Sinch | Mailgun | Latest | HTTPS |
| Cache | Redis Ltd | Redis | Latest | TCP/IP |
| Key Vault | Google Cloud | Secret Manager | Latest | HTTPS |
| Storage | Google Cloud | Firebase Storage | Latest | HTTPS |
| Authentication | Google Cloud | Firebase Auth | Latest | HTTPS |
| Database | Google Cloud | Firebase Firestore | Latest | HTTPS |
| Monitoring | Google Cloud | Cloud Observability | Latest | HTTPS |
| Parameters | Google Cloud | Firebase Remote Config | Latest | HTTPS |
| Backend Platform | Render | Render | Latest | HTTPS |
| Frontend Platform | Vercel | Vercel | Latest | HTTPS |

## Justificación de Selecciones

### Infraestructura Base
- **Cloudflare WAF**: Protección efectiva y escalable contra amenazas web
- **Google Cloud API Gateway**: Gestión centralizada y segura de APIs

### Autenticación y Seguridad
- **Firebase Auth**: Gestión robusta de identidades y accesos
- **Secret Manager**: Gestión segura de credenciales y secretos

### Procesamiento y Datos
- **Stripe Billing**: Sistema completo para pagos recurrentes
- **Redis**: Caché de alto rendimiento para datos frecuentes
- **Firestore**: Base de datos NoSQL escalable y en tiempo real

### Frontend y Desarrollo
- **Vercel**: Plataforma optimizada para Next.js con CDN global
- **Render**: PaaS simple y eficiente para backend

[Ver detalles completos de implementación](./04-arquitectura/implementacion.md)