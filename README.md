# Documento de Arquitectura de Software (DAS) - Nexa

## Índice de Documentación

### 1. Información General
- [Documento Principal de Información](docs/01-informacion-general.md)
  - Control de cambios y revisiones
  - Propósito del proyecto

### 2. Motivadores de la Arquitectura
- [Documento Principal de Motivadores](docs/02-motivadores.md)
- Documentos Detallados:
  - [✏️ Restricciones Técnicas](docs/02-motivadores/2.1-restricciones-tecnicas.md)
  - [✏️ Restricciones de Negocio](docs/02-motivadores/2.2-restricciones-negocio.md)
  - [✏️ Atributos de Calidad](docs/02-motivadores/2.3-atributos-calidad.md)
  - [✏️ Funcionalidades Críticas](docs/02-motivadores/2.4-funcionalidades-criticas.md)

### 3. Arquetipo de Solución
- [Documento Principal de Arquetipo](docs/03-arquetipo.md)
- Documentos Detallados:
  - [✏️ Especificación de Componentes](docs/03-arquetipo/componentes.md)
- Diagramas:
  - [🖼️ Diagrama de Arquetipo](diagramas/arqueotipo.png)

### 4. Arquitectura de Solución
- [Documento Principal de Arquitectura](docs/04-arquitectura.md)
- Documentos Detallados:
  - [✏️ Detalles de Implementación](docs/04-arquitectura/implementacion.md)
- Diagramas:
  - [🖼️ Diagrama de Arquitectura](diagramas/arquitectura.png)

### 5. Línea Base Arquitectónica
- [Documento Principal de Línea Base](docs/05-linea-base.md)
- Documentos Detallados:
  - [✏️ Componentes Adoptados](docs/05-linea-base/componentes-adoptados.md)
  - [✏️ Componentes Desarrollados](docs/05-linea-base/componentes-desarrollados.md)

### 6. Justificación de la Solución
- [Documento de Justificación](docs/06-justificacion.md)

### 7. Vistas de Arquitectura
- [Documento Principal de Vistas](docs/07-vistas.md)

#### 7.1 Vista de Secuencia
- [✏️ Documentación de Secuencias](docs/secuencia.md)
- [🖼️ Diagrama de Secuencia](diagramas/secuencia.png)

#### 7.2 Vista de Paquetes
- [✏️ Documentación de Paquetes Frontend](docs/paquetes_front.md)
- [🖼️ Diagrama de Paquetes Frontend](diagramas/paquete_front.png)
- [✏️ Documentación de Paquetes Backend](docs/paquetes_back.md)
- [🖼️ Diagrama de Paquetes Backend](diagramas/pauqete_back.png)

#### 7.3 Vista de Componentes
- [✏️ Documentación de Componentes Frontend](docs/componentes_front.md)
- [🖼️ Diagrama de Componentes Frontend](diagramas/componentes_front.png)
- [✏️ Documentación de Componentes Backend](docs/componentes_backend.md)
- [🖼️ Diagrama de Componentes Backend](diagramas/componentes_backend.png)

## Leyenda
- ✏️ : Documento de texto con explicaciones detalladas
- 🖼️ : Recurso visual (diagrama, imagen)

## Descripción General

Nexa es una plataforma web SaaS (Software as a Service) diseñada para emprendedores y pequeños negocios que venden productos por redes sociales. Permite digitalizar su tienda sin conocimientos técnicos, ofreciendo organización profesional, gestión de pedidos y visibilidad clara del rendimiento del negocio.

## Propósito de este Documento

Este documento de arquitectura de software (DAS) describe la arquitectura del sistema Nexa, incluyendo decisiones técnicas, componentes, restricciones y justificaciones. La documentación está organizada en secciones para facilitar su mantenimiento y actualización, con clara distinción entre documentos explicativos y recursos visuales.

## Descripción General

Nexa es una plataforma web SaaS (Software as a Service) diseñada para emprendedores y pequeños negocios que venden productos por redes sociales. Permite digitalizar su tienda sin conocimientos técnicos, ofreciendo organización profesional, gestión de pedidos y visibilidad clara del rendimiento del negocio.

## Propósito de este Documento

Este documento de arquitectura de software (DAS) describe la arquitectura del sistema Nexa, incluyendo decisiones técnicas, componentes, restricciones y justificaciones. Está organizado en secciones para facilitar su mantenimiento y actualización.

## Navegación

Cada sección está contenida en su propio archivo para mejor organización y mantenibilidad. Los diagramas se encuentran en la carpeta `diagramas/`.