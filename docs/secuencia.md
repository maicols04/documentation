[🔙 Volver al README](./README.md)

# Diagrama de Secuencia

## Índice
- [Diagrama de Secuencia](#diagrama-de-secuencia)
  - [Índice](#índice)
  - [Descripción General](#descripción-general)
  - [Diagrama](#diagrama)
  - [Líneas de tiempo](#líneas-de-tiempo)
    - [**Interacción**](#interacción)
  - [Flujos Principales](#flujos-principales)
    - [1. Ejecución de Operación](#1-ejecución-de-operación)
    - [2. Manejo de Errores](#2-manejo-de-errores)
    - [3. Capas de la Arquitectura](#3-capas-de-la-arquitectura)

## Descripción General
Este diagrama representa el flujo de interacción entre los diferentes componentes del sistema **Nexa**, siguiendo los principios de **Clean Architecture** y mostrando la separación clara de responsabilidades para la ejecución de una **operación transaccional genérica**.

## Diagrama
![Diagrama de Secuencia](../diagramas/secuencia.png)

## Líneas de tiempo

| **Nombre**     | **Descripción**                                                                              |
| -------------- | -------------------------------------------------------------------------------------------- |
| **Frontend**   | Capa de presentación que inicia la solicitud.                                                |
| **Controller** | Punto de entrada HTTP que recibe la petición del Frontend.                                   |
| **DTO**        | Objeto encargado de transportar y normalizar los datos entre capas.                          |
| **Interactor** | Coordina la ejecución del caso de uso (actúa como orquestador).                              |
| **Factory**    | Responsable de construir el objeto de Dominio a partir del DTO.                              |
| **UseCase**    | Define la lógica de negocio específica y ejecuta las validaciones correspondientes.          |
| **Validator**  | Encargado de asegurar el cumplimiento de las reglas de negocio antes de persistir los datos. |
| **Mapper**     | Convierte el objeto de Dominio en una Entidad lista para persistencia.                       |
| **Repository** | Capa responsable del acceso a datos. Recibe el objeto Entidad para persistirlo.              |

---

### **Interacción**

| **Acción**                            | **Origen** | **Destino** | **Descripción**                                                                                           |
| ------------------------------------- | ---------- | ----------- | --------------------------------------------------------------------------------------------------------- |
| **1. execute(JSON)**                  | Frontend   | Controller  | El cliente inicia la ejecución de la operación, entregando los datos en formato JSON.                    |
| **2. mapJsonToDTO / normalize(JSON)** | Controller | DTO         | El Controller inicia el mapeo y normalización de los datos de entrada.                                    |
| **3. DTO (Normalizado)**              | DTO        | Controller  | El DTO devuelve la información validada y normalizada al Controller.                                      |
| **4. execute(DTO)**                   | Controller | Interactor  | El Controller delega la ejecución de la transacción al Interactor, quien orquesta el flujo completo.      |
| **5. toDomain(DTO)**                  | Interactor | Factory     | El Interactor solicita la creación del objeto de Dominio a partir del DTO.                                |
| **6. Domain Object**                  | Factory    | Interactor  | El Factory devuelve el objeto de Dominio validado en su construcción.                                     |
| **7. execute(Domain)**                | Interactor | UseCase     | El Interactor delega la ejecución del flujo principal al Caso de Uso.                                     |
| **8. execute(Domain)**                | UseCase    | Validator   | El Caso de Uso envía el objeto de Dominio al Validador para comprobar las reglas de negocio.              |
| **9. return exception (si aplica)**   | Validator  | UseCase     | Si las reglas no se cumplen, el Validador genera una excepción que interrumpe la transacción.             |
| **10. toEntity(Domain)**              | UseCase    | Mapper      | Si las validaciones se cumplen, el Caso de Uso convierte el objeto de Dominio en una Entidad persistible. |
| **11. Entity**                        | Mapper     | UseCase     | El Mapper devuelve la Entidad al Caso de Uso.                                                             |
| **12. execute(Entity)**               | UseCase    | Repository  | Se ejecuta la persistencia o acción correspondiente contra la fuente de datos.                            |
| **13. return**                        | Repository | UseCase     | La operación en la capa de datos se completa exitosamente.                                                |
| **14. return**                        | UseCase    | Interactor  | El Caso de Uso notifica al Interactor la finalización del proceso.                                        |
| **15. toDTO(Domain)**                 | Interactor | DTO         | El Interactor mapea el objeto de Dominio resultante a un DTO de salida.                                   |
| **16. return DTO**                    | DTO        | Interactor  | El DTO de respuesta (output) es devuelto al Interactor.                                                   |
| **17. return DTO**                    | Interactor | Controller  | El Interactor propaga el DTO de respuesta al Controller.                                                  |
| **18. return JSON**                   | Controller | Frontend    | El Controller responde al cliente con el JSON finalizado, incluyendo el resultado y estado HTTP adecuado. |

---

## Flujos Principales

### 1. Ejecución de Operación
- Recepción de datos desde el cliente.  
- Normalización y validación inicial.  
- Creación del objeto de dominio.  
- Validación de reglas de negocio.  
- Ejecución de la operación en la capa de datos.  
- Retorno de la respuesta estructurada.

### 2. Manejo de Errores
- Validación de datos de entrada.  
- Excepciones de negocio centralizadas.  
- Uso del catálogo de mensajes para todas las respuestas de error.  
- Respuestas HTTP adecuadas según el tipo de error.

### 3. Capas de la Arquitectura
- Presentación (Frontend)  
- API (Controller)  
- Aplicación (Interactor, UseCase)  
- Dominio (Factory, Validator)  
- Infraestructura (Repository)
