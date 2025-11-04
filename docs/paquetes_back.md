## 📦 Diagrama de Paquetes: nexa backend

| Paquete | Paquete Padre | Descripción | Usa/Importa |
| :--- | :--- | :--- | :--- |
| **co** | — | Paquete raíz que indica que la solución se desarrolla para el país Colombia. | |
| **edu** | co | Paquete que indica que la solución se desarrolla para una compañía del sector educativo. | |
| **uco** | edu | Paquete que indica que la solución se desarrolla para una compañía correspondiente a la Universidad Católica de Oriente (UCO). | |
| **nexa** | uco | Paquete que indica que todos los paquetes que se encuentran dentro de él conforman la solución de un dominio/contexto/aplicación denominada nexa. | |
| **primary** | nexa | Paquete que agrupa todos los elementos de la capa de userinterface de la capa de entrada o driver de una arquitectura limpia. | crosscutting |
| **application** | nexa | Paquete que agrupa todos los elementos de la capa de applicationcore de una arquitectura limpia para la aplicación nexa. | crosscutting |
| **secondary** | nexa | Paquete que agrupa todos los elementos de la capa de infrastructure de una arquitectura limpia para la aplicación nexa y driven. | crosscutting |
| **<<>entity>>** | nexa | Paquete que agrupa los objetos de valor y las entidades clave del Dominio a las que se les realizan transacciones. Sirve como el modelo centralizado. | crosscutting |
| **crosscutting** | nexa | Paquete que agrupa todos los elementos de la capa de crosscutting o transversal de una arquitectura limpia que puede ser usada desde cualquier otro paquete. | |
| **controller** | primary | Paquete que agrupa todas las API de tipo REST de la aplicación nexa. | interactor, dto |
| **interactor** | application | Paquete de la capa de aplicación externa al dominio que orquesta los flujos de negocio y representa la entrada hacia la parte más interna. | |
| **<<>transaction>** | <<>entity>> | Paquete que define el contexto transaccional y agrupa la lógica de negocio que se aplica a cada entidad de nuestra aplicación. | |
| **ports** | secondary | Paquete que agrupa puertos (contratos) para los componentes externos que usa nexa; este puede ser usado por la implementacion del caso de uso. | |
| **adapters** | secondary | Paquete que agrupa implementaciones de los diferentes componentes que usa nexa. | ports |
| **usecase** | application | Paquete de la capa de aplicación externa al dominio que orquesta los flujos de negocio y representa la entrada hacia la parte más interna. | |
| **interactor** | <<transaction>> | Paquete que agrupa elementos de la capa de application domain en clean architecture para nexa. | |
| **notifications** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de notificaciones que va a funcionar con nexa. | notifications |
| **payments** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de pagos que va a funcionar con nexa. | payments |
| **monitoring** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de monitoreo que va a funcionar con nexa. | monitoring |
| **repository** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de manejo de datos que va a funcionar con nexa. | entity, repository |
| **messagecatalog** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de catalogo de mensajes que va a funcionar con nexa. | messagecatalog |
| **parameterscatalog** | ports | Paquete que agrupa contratos, reglas que debe cumplir el componente externo de catalogo de parametros que va a funcionar con nexa. | parameterscatalog |
| **notifications** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de notificaciones. | notifications |
| **payments** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de pagos. | payments |
| **monitoring** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de monitoreo. | monitoring |
| **repository** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de manejo de datos. | repository |
| **messagecatalog** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de catalogo de mensajes. | messagecatalog |
| **parameterscatalog** | adapters | Paquete que representa el componente externo que se va a usar en nexa para el servicio de parametros. | parameterscatalog |
| **interactor** | application | Paquete que agrupa todos los contratos de fachada de la capa de applicationcore de la aplicación nexa. | interactor |
| **usecase** | application | Paquete que agrupa los contratos de los casos de uso de la capa de applicationcore de la aplicación nexa. | interactor |
| **dto** | interactor | Paquete que agrupa objetos de transferencia de datos (DTO) en application core. | usecase |
| **impl** | interactor | Paquete que agrupa las clases concretas que implementa el interactor de la capa application de nexa. | domain, dto, mapper |
| **mapper** | interactor | Paquete que agrupa mapeadores entre DTO y domain. | domain, dto |
| **domain** | usecase | Paquete que agrupa todos los dominios (entidades) de la capa de applicationcore de la aplicación microservice. | |
| **impl** | usecase | Paquete que agrupa todas las implementaciones concretas de los casos de uso de la capa de applicationcore de la aplicación nexa y puede usar el contenido de ports. | entity, ports, domain |
| **mapper** | usecase | Paquete que agrupa mapeadores entre entidades y dominio. | entity, domain |