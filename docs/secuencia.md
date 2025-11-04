**Diagrama de secuencia**


**Líneas de tiempo**

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

**Interacción**

| **Acción**                            | **Origen** | **Destino** | **Descripción**                                                                                           |
| ------------------------------------- | ---------- | ----------- | --------------------------------------------------------------------------------------------------------- |
| **1. POST /user(JSON)**               | Frontend   | Controller  | El cliente realiza una solicitud para crear un usuario, entregando los datos en formato JSON.             |
| **2. mapJsonToDTO / normalize(JSON)** | Controller | DTO         | El Controller inicia el proceso de mapeo y normalización de los datos recibidos.                          |
| **3. DTO (Normalizado)**              | DTO        | Controller  | El DTO devuelve la información validada y normalizada al Controller.                                      |
| **4. execute(DTO)**                   | Controller | Interactor  | El Controller delega la ejecución de la transacción al Interactor, quien inicia la orquestación.          |
| **5. toDomain(DTO)**                  | Interactor | Factory     | El Interactor solicita la creación del objeto de Dominio a partir del DTO.                                |
| **6. Domain Object**                  | Factory    | Interactor  | El Factory devuelve el objeto de Dominio validado en su construcción.                                     |
| **7. execute(Domain)**                | Interactor | UseCase     | El Interactor delega la ejecución del flujo principal al Caso de Uso.                                     |
| **8. execute(Domain)**                | UseCase    | Validator   | El Caso de Uso envía el objeto de Dominio al Validador para comprobar las reglas de negocio.              |
| **9. return exception (si aplica)**   | Validator  | UseCase     | Si las reglas no se cumplen, el Validador genera una excepción que interrumpe la transacción.             |
| **10. toEntity(Domain)**              | UseCase    | Mapper      | Si las validaciones se cumplen, el Caso de Uso convierte el objeto de Dominio en una Entidad persistible. |
| **11. Entity**                        | Mapper     | UseCase     | El Mapper devuelve la Entidad al Caso de Uso.                                                             |
| **12. execute(Entity)**               | UseCase    | Repository  | Se ejecuta la persistencia de la Entidad contra la fuente de datos.                                       |
| **13. return void**                   | Repository | UseCase     | La operación de persistencia se completa exitosamente.                                                    |
| **14. return void**                   | UseCase    | Interactor  | El Caso de Uso notifica al Interactor la finalización exitosa.                                            |
| **15. return void**                   | Interactor | Controller  | El Interactor confirma al Controller que la transacción fue completada.                                   |
| **16. return 201 Created**            | Controller | Frontend    | La API responde al cliente confirmando la creación exitosa del usuario.                                   |
