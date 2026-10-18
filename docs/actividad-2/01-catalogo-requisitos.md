# 01. Catálogo de requisitos

## 1. Objetivo

Identificar y documentar los requisitos funcionales y los atributos de calidad de la plataforma logística, con el propósito de orientar las decisiones arquitectónicas y establecer criterios que permitan verificar el cumplimiento de las necesidades del negocio.

## 2. Requisitos funcionales

Los requisitos funcionales describen las operaciones que debe permitir la plataforma logística.

| Código | Requisito | Descripción | Prioridad |
|---|---|---|---|
| RF-01 | Gestión de pedidos | El sistema debe permitir registrar y consultar los pedidos logísticos. | Alta |
| RF-02 | Gestión de inventario | El sistema debe permitir consultar y actualizar la disponibilidad de productos. | Alta |
| RF-03 | Gestión de entregas | El sistema debe permitir asignar entregas y consultar su estado. | Alta |
| RF-04 | Seguimiento de pedidos | El sistema debe permitir conocer el estado y la trazabilidad de un pedido. | Alta |
| RF-05 | Gestión de incidencias | El sistema debe permitir registrar y consultar problemas relacionados con pedidos y entregas. | Media |
| RF-06 | Consulta de información | El sistema debe permitir consultar la información logística necesaria para la operación. | Media |
| RF-07 | Gestión de usuarios | El sistema debe permitir identificar a los usuarios y controlar sus permisos de acceso. | Alta |

## 3. Atributos de calidad

Los atributos de calidad establecen las condiciones que debe cumplir la solución para funcionar de manera confiable y facilitar su evolución.

| Código | Atributo | Descripción | Prioridad |
|---|---|---|---|
| RNF-01 | Rendimiento | Las consultas de pedidos deben responder en un tiempo adecuado para la operación. | Alta |
| RNF-02 | Seguridad | La información debe protegerse mediante autenticación, autorización y controles de acceso. | Alta |
| RNF-03 | Disponibilidad | El sistema debe estar disponible durante los periodos requeridos por la operación logística. | Alta |
| RNF-04 | Mantenibilidad | El código debe organizarse en módulos con responsabilidades claramente definidas. | Alta |
| RNF-05 | Escalabilidad | La arquitectura debe permitir ampliar la capacidad cuando aumente la demanda. | Media |
| RNF-06 | Evolución | Los cambios en las reglas de negocio deben poder realizarse sin afectar innecesariamente otros módulos. | Alta |
| RNF-07 | Integridad de datos | Las operaciones deben mantener la consistencia de la información de pedidos, inventario y entregas. | Alta |

## 4. Restricciones identificadas

Las siguientes restricciones iniciales deberán confirmarse con el diagnóstico de la Actividad 1 y las condiciones reales del proyecto.

- La solución debe responder a las necesidades del negocio logístico.
- La arquitectura debe mantener una separación clara de responsabilidades.
- La implementación debe considerar los costos de desarrollo, infraestructura y mantenimiento.
- La solución debe permitir verificar el cumplimiento de los requisitos.
- La complejidad técnica debe ser proporcional al tamaño y las necesidades de la operación.

## 5. Criterios generales de aceptación

- Los requisitos funcionales deben poder comprobarse mediante pruebas.
- Los atributos de calidad deben contar con métricas o condiciones de verificación.
- Los módulos deben tener responsabilidades claramente identificadas.
- Las decisiones arquitectónicas deben justificarse a partir de las necesidades del negocio.
- Los riesgos y las limitaciones de la solución deben quedar documentados.

## 6. Observación

Este catálogo constituye una propuesta inicial para la plataforma logística. Las prioridades y los requisitos deberán validarse con el diagnóstico del problema, los actores, el alcance y los riesgos identificados en la Actividad 1 antes de considerarse definitivos.