# 04. Comparación de alternativas arquitectónicas

## 1. Objetivo

Comparar dos alternativas estructurales para la plataforma logística, evaluando sus ventajas, limitaciones, costos, complejidad y capacidad de responder a los requisitos funcionales y atributos de calidad identificados.

## 2. Alternativa A: Monolito modular

Consiste en desarrollar una aplicación que agrupa las funcionalidades en módulos internos con responsabilidades claramente definidas. Los módulos comparten el despliegue de la aplicación, pero mantienen una separación lógica de sus funciones.

### Ventajas

- Menor complejidad operativa inicial.
- Implementación y despliegue más sencillos.
- Menores costos iniciales de infraestructura.
- Facilidad para probar operaciones que involucran varios módulos.
- Permite separar pedidos, inventario, entregas e incidencias por responsabilidades.

### Desventajas

- Un error grave puede afectar a toda la aplicación.
- Los módulos pueden acoplarse si no se respetan sus límites.
- El escalamiento independiente de cada módulo es limitado.
- Una base de código que crece sin control puede dificultar el mantenimiento.

## 3. Alternativa B: Arquitectura distribuida por servicios

Consiste en dividir la plataforma en servicios independientes, organizados por dominios de negocio, que se comunican mediante contratos o interfaces definidos.

### Ventajas

- Permite desplegar y escalar servicios de manera independiente.
- Facilita aislar determinados fallos entre servicios.
- Favorece la autonomía de los equipos de desarrollo.
- Permite integrar sistemas externos mediante interfaces definidas.
- Facilita la evolución independiente de dominios cuando existen necesidades diferenciadas.

### Desventajas

- Mayor complejidad de infraestructura y operación.
- Requiere gestionar la comunicación entre servicios.
- Puede introducir problemas de latencia y fallos de red.
- Exige mayor atención a la observabilidad, seguridad y manejo de errores.
- Puede incrementar los costos de desarrollo y mantenimiento.

## 4. Matriz comparativa

| Criterio | Monolito modular | Arquitectura distribuida |
|---|---|---|
| Costo inicial | Bajo a medio | Medio a alto |
| Complejidad operativa | Baja a media | Alta |
| Velocidad de implementación inicial | Alta | Media o baja |
| Facilidad de mantenimiento | Alta si existen límites claros | Alta si los servicios están bien diseñados |
| Escalamiento independiente | Limitado | Alto |
| Comunicación entre módulos | Principalmente interna | Mediante comunicación entre servicios |
| Aislamiento de fallos | Más limitado | Puede ser mayor, según el diseño |
| Integración con sistemas externos | Posible mediante interfaces | Posible mediante interfaces y servicios |
| Requisitos de infraestructura | Menores inicialmente | Mayores inicialmente |
| Adecuación para un proyecto de crecimiento moderado | Alta | Puede resultar excesiva |
| Complejidad de pruebas y despliegue | Menor | Mayor |

## 5. Análisis técnico y de negocio

El monolito modular permite organizar las funcionalidades de la plataforma logística sin introducir desde el inicio la complejidad de múltiples despliegues. Esta opción favorece una implementación inicial más sencilla y permite establecer límites claros entre pedidos, inventario, entregas e incidencias.

La arquitectura distribuida ofrece ventajas cuando los dominios necesitan escalar de forma independiente, existen equipos autónomos o la operación requiere aislar determinados fallos. Sin embargo, también introduce desafíos relacionados con la comunicación entre servicios, la observabilidad, la consistencia de datos y la infraestructura.

La decisión debe considerar el tamaño actual del proyecto, la experiencia del equipo, el presupuesto disponible y el crecimiento esperado. No se debe seleccionar una arquitectura distribuida únicamente por ser más compleja o moderna.

## 6. Alternativa recomendada inicialmente

Se propone considerar el monolito modular como alternativa inicial para la plataforma logística, siempre que el diagnóstico de la Actividad 1 confirme que el tamaño, la demanda y los recursos disponibles permiten esta elección.

La recomendación se fundamenta en reducir la complejidad operativa inicial, facilitar la implementación y mantener una separación clara de responsabilidades.

La arquitectura distribuida se conserva como alternativa futura si existen evidencias de que determinados dominios requieren escalamiento independiente, despliegues autónomos o aislamiento operativo.

## 7. Riesgos y trade-offs

### Monolito modular

- **Riesgo:** que los módulos pierdan su independencia lógica y se genere acoplamiento.
- **Mitigación:** establecer límites de módulos, contratos internos y pruebas automatizadas.
- **Trade-off:** se acepta compartir el despliegue a cambio de reducir la complejidad inicial.

### Arquitectura distribuida

- **Riesgo:** aumentar los costos y la complejidad antes de que exista una necesidad real.
- **Mitigación:** distribuir servicios únicamente cuando existan requisitos que lo justifiquen.
- **Trade-off:** se acepta mayor complejidad operativa a cambio de una mayor independencia de despliegue y escalamiento.

## 8. Conclusión

La comparación muestra que ambas alternativas pueden responder a las necesidades de una plataforma logística, pero presentan diferentes costos y riesgos. El monolito modular constituye una recomendación inicial razonable cuando se busca implementar el sistema con menor complejidad y conservar una estructura organizada.

La decisión definitiva deberá validarse con los requisitos, las restricciones y los riesgos identificados en la Actividad 1.