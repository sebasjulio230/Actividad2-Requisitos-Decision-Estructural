# 02. Matriz de priorización de requisitos

## 1. Objetivo

Priorizar los requisitos de la plataforma logística considerando su importancia para el negocio, su impacto en la arquitectura y la complejidad de implementación.

## 2. Escala de evaluación

Se utilizará una escala de 1 a 3 para evaluar cada criterio.

| Valor | Impacto en el negocio | Impacto arquitectónico | Complejidad |
|---|---|---|---|
| 1 | Bajo | Bajo | Baja |
| 2 | Medio | Medio | Media |
| 3 | Alto | Alto | Alta |

La prioridad se establece según la importancia del requisito para la operación. La complejidad representa el esfuerzo estimado para implementarlo, no su importancia.

## 3. Matriz de priorización

| Código | Requisito | Impacto en el negocio | Impacto arquitectónico | Complejidad | Prioridad |
|---|---|---:|---:|---:|---|
| RF-01 | Gestión de pedidos | 3 | 3 | 2 | Alta |
| RF-02 | Gestión de inventario | 3 | 3 | 3 | Alta |
| RF-03 | Gestión de entregas | 3 | 3 | 3 | Alta |
| RF-04 | Seguimiento de pedidos | 3 | 2 | 2 | Alta |
| RF-05 | Gestión de incidencias | 2 | 2 | 2 | Media |
| RF-06 | Consulta de información | 2 | 1 | 1 | Media |
| RF-07 | Gestión de usuarios | 3 | 3 | 2 | Alta |
| RNF-01 | Rendimiento | 3 | 3 | 2 | Alta |
| RNF-02 | Seguridad | 3 | 3 | 3 | Alta |
| RNF-03 | Disponibilidad | 3 | 3 | 3 | Alta |
| RNF-04 | Mantenibilidad | 2 | 3 | 2 | Alta |
| RNF-05 | Escalabilidad | 2 | 3 | 3 | Media |
| RNF-06 | Evolución | 2 | 3 | 2 | Alta |
| RNF-07 | Integridad de datos | 3 | 3 | 3 | Alta |

## 4. Análisis de los resultados

Los requisitos de gestión de pedidos, inventario y entregas tienen prioridad alta porque representan operaciones centrales de la plataforma logística. Su impacto arquitectónico también es alto, ya que requieren definir responsabilidades, relaciones entre módulos y reglas de negocio.

La seguridad, la disponibilidad, el rendimiento y la integridad de los datos son atributos esenciales para proteger la información y mantener la continuidad de las operaciones.

La mantenibilidad y la facilidad de evolución también deben considerarse desde el diseño inicial, con el fin de reducir el acoplamiento y facilitar futuros cambios.

La escalabilidad se considera de prioridad media en esta evaluación inicial. Su importancia deberá revisarse según el crecimiento esperado de la operación y la demanda prevista.

## 5. Implicaciones para la arquitectura

La priorización sugiere que la solución debe:

- Separar claramente los módulos de pedidos, inventario, entregas e incidencias.
- Proteger los accesos y la información del sistema.
- Mantener la consistencia de los datos entre las operaciones relacionadas.
- Facilitar el mantenimiento y los cambios en las reglas de negocio.
- Evitar una complejidad operativa que no esté justificada por las necesidades actuales.

## 6. Observación

Los valores de esta matriz son estimaciones iniciales para orientar el análisis arquitectónico. Deben validarse con el diagnóstico de la Actividad 1 y con las necesidades reales de los actores del sistema.