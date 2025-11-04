## 🛠️ Diagrama de Componentes para el Componente: Nexa backend

Descripción: Diagrama que muestra el 100% de los componentes que serán construidos o adoptados para proceder con la construcción del componente indicado. Adicionalmente, indica cómo estos componentes están relacionados.


| **Componente** | **Estereotipo / Versión** | **Descripción** | **Motivación** | **Depende / Usa** | **Tipo** |
| --------------- | -------------------------- | ---------------- | ---------------- | ------------------ | -------- |
| **Nexa** | <<>dist>> nexa | Componente que representa el backend de la aplicación **Nexa** que publica todos los servicios de negocio que está en la capacidad de ofrecer. Contiene toda la lógica de la aplicación que va a ser ofrecida por medio de servicios REST. | Artefacto distribuible final de la solución de backend. | **Nest.js 11.1.6**, **Node.js 22** | **Componente Propio a desarrollar** |
| **Nest.js 11.1.6** | <<>framework/project>> nest.js 11.1.6 | Framework usado para acelerar el desarrollo de una aplicación, respecto a aquellos aspectos que no hacen parte del core base o principal de negocio. | Acelerar el desarrollo y concentrar los esfuerzos del equipo en tareas y aspectos netamente del negocio. | **Node.js 22** | **Componente Externo (Framework/Acelerador)** |
| **Node.js 22** | <<>runtime>> node.js 22 | Ambiente de ejecución (Runtime) basado en el motor **V8** que ejecuta el código JavaScript (transpilado desde TypeScript). Es la plataforma base para el backend. | Plataforma base que provee el runtime y las librerías Core necesarias para la ejecución del framework y la aplicación con prestaciones de rendimiento y concurrencia. | — | **Componente Externo (Runtime)** |
