[🔙 Volver al README](./README.md)

# Justificación de la Solución

## Justificación General

La arquitectura de Nexa se diseñó pensando en emprendedores reales: personas que necesitan una plataforma confiable, que crezca con ellos y que no les complique la vida. Por eso se eligieron herramientas modernas en la nube que permiten escalar fácilmente, mantener los costos bajo control y ofrecer una experiencia segura para todos.

## Componentes Clave y su Justificación

### Infraestructura Base

- **Cloudflare WAF**: Protege la plataforma de ataques sin que el usuario tenga que preocuparse.
- **Google Cloud API Gateway**: Organiza todo lo que pasa entre el frontend y el backend, como si fuera un centro de control.
- **Firebase Auth**: Permite que los usuarios inicien sesión de forma segura, sin tener que construir todo desde cero.

### Procesamiento y Datos

- **Stripe**: Se encarga de los pagos y suscripciones, con confianza y sin complicaciones.
- **Redis**: Acelera la plataforma, guardando datos temporales para que todo cargue más rápido.
- **Firestore**: Guarda la información de forma flexible y en tiempo real, ideal para una plataforma dinámica.

### Frontend y Backend

- **Nuxt.js**: Permite que el sitio cargue rápido y se vea bien en buscadores.
- **NestJS**: Organiza el backend como si fuera una caja de herramientas bien ordenada.
- **TypeScript**: Ayuda a que el código sea más claro y fácil de mantener.

## Ventajas

1. **Escalabilidad**
   - La infraestructura se adapta si Nexa crece.
   - No hay necesidad de rehacer todo.
   - Se ajusta automáticamente a la demanda.

2. **Costos**
   - Se paga solo por lo que se usa.
   - No hay gastos innecesarios.
   - Los costos son predecibles.

3. **Desarrollo**
   - El equipo puede avanzar rápido.
   - Se usan herramientas probadas.
   - El ecosistema es confiable.

4. **Mantenibilidad**
   - El código está bien organizado.
   - Es fácil hacer cambios sin romper nada.
   - Se puede probar y mejorar continuamente.

## Desventajas

1. **Dependencia de Proveedores**
   - Puede haber cambios en precios o servicios.
   - Existe el riesgo de quedar atado a un proveedor.

2. **Complejidad**
   - Al principio puede parecer complicado.
   - Requiere integrar varios servicios.

3. **Costos Variables**
   - El crecimiento puede aumentar los costos.
   - Hay que vigilar el uso de red y almacenamiento.

## Mitigación de Riesgos

1. **Vendor Lock-in**
   - Se usa una arquitectura modular.
   - Se definen interfaces claras.
   - Se documenta todo para facilitar cambios.

2. **Complejidad**
   - Se ofrece capacitación continua.
   - La documentación es clara y accesible.
   - Se implementa monitoreo robusto.

3. **Costos**
   - Se hace seguimiento detallado del presupuesto.
   - Se configuran alertas de uso.
   - Se optimiza constantemente la infraestructura.