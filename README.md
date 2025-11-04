# Documento de Arquitectura de Software (DAS) - Nexa

## Índice

1. [Información General](docs/01-informacion-general.md)
   - Control de cambios y revisiones
   - Propósito del proyecto

2. [Motivadores de la Arquitectura](docs/02-motivadores.md)
   - [Restricciones técnicas](docs/02-motivadores/2.1-restricciones-tecnicas.md)
   - [Restricciones de negocio](docs/02-motivadores/2.2-restricciones-negocio.md)
   - [Atributos de calidad](docs/02-motivadores/2.3-atributos-calidad.md)
   - [Funcionalidades críticas](docs/02-motivadores/2.4-funcionalidades-criticas.md)

3. [Arquetipo de Solución](docs/03-arquetipo.md)
   - [Componentes](docs/03-arquetipo/componentes.md)
   - [Diagrama de Arquetipo](diagramas/arqueotipo.png)

4. [Arquitectura de Solución](docs/04-arquitectura.md)
   - [Detalles de Implementación](docs/04-arquitectura/implementacion.md)
   - [Diagrama de Arquitectura](diagramas/arquitectura.png)

5. [Línea Base Arquitectónica](docs/05-linea-base.md)
   - [Componentes Adoptados](docs/05-linea-base/componentes-adoptados.md)
   - [Componentes Desarrollados](docs/05-linea-base/componentes-desarrollados.md)

6. [Justificación de la Solución](docs/06-justificacion.md)

7. [Vistas de Arquitectura](docs/07-vistas.md)
   - [Vista de Secuencia](docs/secuencia.md)
   - [Vista de Paquetes Frontend](docs/paquetes_front.md)
   - [Vista de Paquetes Backend](docs/paquetes_back.md)
   - [Vista de Componentes Frontend](docs/componentes_front.md)
   - [Vista de Componentes Backend](docs/componentes_backend.md)
   
## Diagramas y Recursos Visuales

### Diagramas de Componentes
- [Componentes Backend](diagramas/componentes_backend.png)
- [Componentes Frontend](diagramas/componentes_front.png)

### Diagramas de Paquetes
- [Paquetes Backend](diagramas/pauqete_back.png)
- [Paquetes Frontend](diagramas/paquete_front.png)

### Diagramas de Secuencia
- [Diagrama de Secuencia General](diagramas/secuencia.png)

### Diagramas de Arquitectura
- [Arquetipo de Referencia](diagramas/arqueotipo.png)
- [Arquitectura del Sistema](diagramas/arquitectura.png)

## Descripción General

Nexa es una plataforma web SaaS (Software as a Service) diseñada para emprendedores y pequeños negocios que venden productos por redes sociales. Permite digitalizar su tienda sin conocimientos técnicos, ofreciendo organización profesional, gestión de pedidos y visibilidad clara del rendimiento del negocio.

## Propósito de este Documento

Este documento de arquitectura de software (DAS) describe la arquitectura del sistema Nexa, incluyendo decisiones técnicas, componentes, restricciones y justificaciones. Está organizado en secciones para facilitar su mantenimiento y actualización.

## Navegación

Cada sección está contenida en su propio archivo para mejor organización y mantenibilidad. Los diagramas se encuentran en la carpeta `diagramas/`.