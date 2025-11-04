# 7. Vistas de Arquitectura

## Vista Funcional

### Diagramas Relacionados
- [Diagrama de Secuencia](../diagramas/secuencia.png)
- [Diagrama de Arquitectura](../diagramas/arquitectura.png)

### Casos de Uso Principales

1. **Gestión de Tienda**
   - Crear tienda
   - Configurar tienda
   - Gestionar productos
   - Ver estadísticas

2. **Gestión de Pedidos**
   - Recibir pedidos
   - Procesar pedidos
   - Actualizar estado
   - Notificar clientes

3. **Suscripciones**
   - Activar suscripción
   - Gestionar pagos
   - Renovar automáticamente
   - Cancelar suscripción


## Vista de Despliegue

### Componentes Principales

1. **Frontend Layer**
   - Vercel CDN
   - Nuxt.js SSR

2. **API Layer**
   - Google Cloud API Gateway
   - NestJS services

3. **Data Layer**
   - Firestore
   - Redis Cache
   - Firebase Storage

[Ver diagrama arquetipo](./diagramas/arqueotipo_referencia.png)

## Vista de Procesos

### Flujos Principales

1. **Registro de Usuario**
2. **Creación de Tienda**
3. **Proceso de Compra**
4. **Gestión de Suscripción**

[Ver diagramas de secuencia](./07-vistas/procesos.md)