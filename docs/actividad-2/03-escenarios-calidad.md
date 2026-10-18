# 03. Escenarios de calidad

## 1. Objetivo

Definir escenarios verificables que permitan evaluar si la arquitectura propuesta para la plataforma logística cumple con los atributos de calidad requeridos por el negocio.

## 2. Escenarios de calidad

### EC-01. Rendimiento en la consulta de pedidos

- **Atributo:** Rendimiento.
- **Estímulo:** Un usuario solicita consultar un pedido.
- **Condición:** El sistema se encuentra en operación normal.
- **Respuesta esperada:** El sistema consulta y presenta la información del pedido.
- **Métrica:** El 95 % de las consultas debe responder en un máximo de 2 segundos.
- **Verificación:** Ejecutar pruebas de rendimiento y medir los tiempos de respuesta.

### EC-02. Seguridad en el acceso

- **Atributo:** Seguridad.
- **Estímulo:** Un usuario intenta ingresar a una funcionalidad protegida.
- **Condición:** El usuario no cuenta con una sesión válida o no tiene los permisos necesarios.
- **Respuesta esperada:** El sistema debe impedir el acceso no autorizado.
- **Métrica:** El 100 % de los casos de prueba de acceso no autorizado debe ser rechazado.
- **Verificación:** Realizar pruebas de autenticación y autorización.

### EC-03. Disponibilidad del sistema

- **Atributo:** Disponibilidad.
- **Estímulo:** Un usuario solicita utilizar la plataforma durante el horario de operación.
- **Condición:** La infraestructura y los servicios se encuentran desplegados.
- **Respuesta esperada:** La plataforma debe estar disponible para procesar solicitudes.
- **Métrica:** Disponibilidad mensual objetivo del 99,5 %.
- **Verificación:** Registrar el tiempo de funcionamiento y las interrupciones durante un periodo mensual.

### EC-04. Integridad de la información

- **Atributo:** Integridad de datos.
- **Estímulo:** Se registra o actualiza un pedido relacionado con una operación logística.
- **Condición:** Existen datos relacionados con el pedido, el inventario o la entrega.
- **Respuesta esperada:** Las operaciones deben respetar las reglas de negocio y mantener la consistencia de los datos.
- **Métrica:** El 100 % de los casos de prueba de integridad debe cumplir las reglas definidas.
- **Verificación:** Ejecutar pruebas sobre las operaciones de registro, actualización y consulta.

### EC-05. Facilidad de mantenimiento

- **Atributo:** Mantenibilidad.
- **Estímulo:** Se solicita modificar una regla de negocio de un módulo.
- **Condición:** Los módulos tienen responsabilidades y límites claramente definidos.
- **Respuesta esperada:** El cambio debe poder implementarse sin modificar innecesariamente módulos no relacionados.
- **Métrica:** Una modificación aislada de una regla de negocio no debe requerir cambios en módulos ajenos, salvo que exista una dependencia justificada.
- **Verificación:** Revisar el código y ejecutar pruebas de regresión después de modificar una regla.

### EC-06. Capacidad de crecimiento

- **Atributo:** Escalabilidad.
- **Estímulo:** Aumenta el número de solicitudes de consulta y seguimiento.
- **Condición:** La plataforma recibe una carga superior a la habitual.
- **Respuesta esperada:** El sistema debe mantener tiempos de respuesta aceptables o permitir ampliar sus recursos.
- **Métrica:** Mantener el objetivo de respuesta de 2 segundos para el 95 % de las consultas bajo la carga de prueba definida.
- **Verificación:** Ejecutar pruebas de carga con distintos niveles de concurrencia y registrar los resultados.

## 3. Consideraciones de validación

Las métricas propuestas son objetivos iniciales de diseño y no resultados de pruebas realizadas. Deben validarse con las necesidades del negocio, la infraestructura disponible y la carga esperada de la plataforma logística.

Los escenarios deberán utilizarse para evaluar las alternativas arquitectónicas y comprobar si la decisión seleccionada responde a los requisitos prioritarios.

## 4. Resultado esperado

La definición de escenarios de calidad permite transformar atributos generales en condiciones medibles. Esto facilita comparar alternativas arquitectónicas, identificar riesgos y establecer pruebas para validar la solución durante su construcción.