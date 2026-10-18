# 05. Criterios de verificación

## 1. Objetivo

Establecer criterios verificables que permitan evaluar el cumplimiento de los requisitos funcionales y los atributos de calidad de la plataforma logística, así como comprobar que la arquitectura seleccionada responde a las necesidades del negocio.

## 2. Criterios de verificación funcional

| Código | Criterio | Método de verificación | Condición de aceptación |
|---|---|---|---|
| CV-01 | Gestión de pedidos | Pruebas funcionales | Se pueden registrar y consultar pedidos correctamente. |
| CV-02 | Gestión de inventario | Pruebas funcionales | Se puede consultar y actualizar la disponibilidad según las reglas del negocio. |
| CV-03 | Gestión de entregas | Pruebas funcionales | Se pueden asignar entregas y consultar sus estados. |
| CV-04 | Seguimiento de pedidos | Pruebas funcionales | La información presentada corresponde al estado registrado del pedido. |
| CV-05 | Gestión de incidencias | Pruebas funcionales | Se pueden registrar y consultar incidencias. |
| CV-06 | Gestión de usuarios | Pruebas de acceso | Los usuarios solo pueden acceder a las funcionalidades autorizadas. |

## 3. Criterios de verificación de calidad

| Código | Atributo | Método de verificación | Condición de aceptación |
|---|---|---|---|
| CV-07 | Rendimiento | Pruebas de carga y medición de tiempos | El 95 % de las consultas de pedidos responde en un máximo de 2 segundos bajo la carga definida. |
| CV-08 | Seguridad | Pruebas de autenticación y autorización | Todos los intentos de acceso no autorizado incluidos en las pruebas son rechazados. |
| CV-09 | Disponibilidad | Monitoreo durante un periodo mensual | Se alcanza el objetivo inicial de disponibilidad del 99,5 %. |
| CV-10 | Integridad de datos | Pruebas de consistencia | Todas las operaciones de prueba respetan las reglas de integridad definidas. |
| CV-11 | Mantenibilidad | Revisión de módulos y pruebas de regresión | Los módulos mantienen responsabilidades claras y los cambios no afectan funcionalidades ajenas sin justificación. |
| CV-12 | Escalabilidad | Pruebas con diferentes niveles de carga | El sistema cumple los objetivos de rendimiento establecidos para cada nivel de carga. |

## 4. Criterios de verificación arquitectónica

La arquitectura deberá cumplir las siguientes condiciones:

- Los módulos de pedidos, inventario, entregas e incidencias deben tener responsabilidades identificables.
- Las dependencias entre módulos deben estar justificadas y documentadas.
- Los contratos o interfaces entre componentes deben estar definidos cuando corresponda.
- Los mecanismos de seguridad deben aplicarse a las operaciones protegidas.
- Las pruebas deben permitir identificar incumplimientos de los requisitos.
- Los cambios de reglas de negocio deben poder realizarse sin modificar innecesariamente componentes no relacionados.

## 5. Evidencias de verificación

Para demostrar el cumplimiento de los criterios se podrán utilizar:

- Resultados de pruebas funcionales.
- Informes de pruebas de rendimiento.
- Registros de intentos de acceso autorizados y no autorizados.
- Registros de disponibilidad.
- Resultados de pruebas de integridad de datos.
- Revisiones de código y pruebas de regresión.
- Documentación de los módulos y sus dependencias.

## 6. Condiciones y limitaciones

Los valores de rendimiento y disponibilidad son objetivos iniciales propuestos, no resultados obtenidos. Para validarlos es necesario definir la carga de prueba, el entorno de ejecución y el periodo de medición.

Los criterios funcionales también deben contrastarse con los requisitos definitivos del negocio antes de implementar las pruebas.

## 7. Resultado esperado

La aplicación de estos criterios permitirá comprobar si la solución arquitectónica responde a los requisitos prioritarios y facilitará la identificación de ajustes necesarios durante el diseño y la construcción de la plataforma logística.