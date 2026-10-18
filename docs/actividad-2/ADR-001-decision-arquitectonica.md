# ADR-001. Decisión arquitectónica de la plataforma logística

## 1. Información general

- **Identificador:** ADR-001.
- **Título:** Selección de la arquitectura inicial de la plataforma logística.
- **Estado:** Propuesta pendiente de validación.
- **Contexto:** Actividad 2. Requisitos y decisión estructural.
- **Fecha:** 18 de octubre de 2026.

## 2. Contexto y problema

La plataforma logística requiere organizar las funcionalidades relacionadas con pedidos, inventario, entregas, seguimiento e incidencias. La arquitectura debe permitir mantener responsabilidades claras, proteger la información y facilitar la evolución del sistema.

La decisión debe considerar los requisitos funcionales, los atributos de calidad, los costos de implementación, la complejidad operativa y los riesgos asociados con cada alternativa.

## 3. Decisión propuesta

Se propone utilizar inicialmente una **arquitectura de monolito modular**, con módulos organizados por responsabilidades del dominio logístico y límites explícitos entre ellos.

La propuesta busca reducir la complejidad operativa inicial y facilitar el desarrollo y mantenimiento del sistema, sin renunciar a una organización que permita evolucionar posteriormente.

Esta decisión queda pendiente de validación con el diagnóstico de la Actividad 1 y las restricciones reales del proyecto.

## 4. Alternativas consideradas

### Alternativa A. Monolito modular

Consiste en una aplicación desplegada como una unidad, organizada internamente en módulos con responsabilidades diferenciadas.

**Ventajas:**
- Menor complejidad de despliegue y operación.
- Menores necesidades iniciales de infraestructura.
- Facilidad para probar funcionalidades relacionadas.
- Separación lógica de los dominios del negocio.

**Desventajas:**
- Los módulos comparten el ciclo de despliegue.
- Un problema general de la aplicación puede afectar varias funcionalidades.
- El crecimiento descontrolado puede generar acoplamiento.

### Alternativa B. Arquitectura distribuida por servicios

Consiste en separar las funcionalidades en servicios independientes que se comunican mediante contratos definidos.

**Ventajas:**
- Permite escalar servicios de forma independiente.
- Favorece despliegues autónomos.
- Puede mejorar el aislamiento de fallos cuando se diseña correctamente.
- Facilita la autonomía de equipos y dominios.

**Desventajas:**
- Mayor complejidad operativa.
- Necesidad de gestionar comunicaciones de red y fallos entre servicios.
- Mayor esfuerzo de observabilidad, seguridad y pruebas.
- Posible incremento de costos de infraestructura y mantenimiento.

## 5. Justificación

La alternativa del monolito modular se propone como punto de partida porque permite organizar los dominios logísticos sin introducir desde el inicio las exigencias de una arquitectura distribuida.

La separación interna en módulos facilita mantener responsabilidades claras y reduce el riesgo de que toda la lógica del negocio quede mezclada en una única estructura sin organización.

La arquitectura distribuida se considera una alternativa válida para escenarios en los que existan necesidades demostrables de escalamiento independiente, despliegues autónomos o aislamiento operativo.

La decisión definitiva deberá contrastarse con el alcance, los actores, los riesgos y las restricciones identificados en la Actividad 1.

## 6. Consecuencias de la decisión

### Consecuencias positivas

- Menor complejidad de operación inicial.
- Organización explícita de las funcionalidades.
- Facilidad para realizar pruebas integradas.
- Menores necesidades iniciales de infraestructura.
- Posibilidad de evolucionar la estructura cuando cambien las necesidades.

### Consecuencias negativas

- No permite desplegar cada módulo de manera independiente.
- La aplicación puede convertirse en una estructura acoplada si no se respetan los límites.
- El escalamiento de una funcionalidad puede requerir ampliar recursos para toda la aplicación.

## 7. Riesgos y medidas de mitigación

| Riesgo | Impacto | Medida de mitigación |
|---|---|---|
| Acoplamiento entre módulos | Alto | Definir responsabilidades, interfaces y reglas de dependencia. |
| Crecimiento descontrolado del código | Medio | Revisar periódicamente la estructura y aplicar pruebas automatizadas. |
| Fallos que afecten varias funcionalidades | Alto | Incorporar manejo de errores, monitoreo y pruebas de recuperación. |
| Aumento de la demanda | Medio | Medir el rendimiento y revisar la capacidad de infraestructura. |
| Necesidad futura de separar servicios | Medio | Mantener límites de dominio claros y contratos bien definidos. |

## 8. Condiciones para reconsiderar la decisión

La decisión deberá revisarse si se identifica alguna de las siguientes condiciones:

- Un módulo requiere escalar independientemente de los demás.
- Los tiempos de despliegue afectan de forma significativa la operación.
- Existen equipos que necesitan trabajar y desplegar de manera autónoma.
- Los requisitos de disponibilidad justifican aislar determinados componentes.
- Las pruebas de carga muestran que la arquitectura no satisface los objetivos establecidos.

## 9. Criterios para validar la decisión

La propuesta se considerará adecuada cuando se compruebe que:

- Los módulos representan responsabilidades diferenciadas.
- Los requisitos funcionales prioritarios pueden satisfacerse.
- Se cumplen los objetivos de rendimiento y seguridad definidos.
- Los costos y la complejidad operativa son compatibles con las restricciones del proyecto.
- Los escenarios de calidad pueden verificarse mediante pruebas.
- Los riesgos identificados cuentan con medidas de mitigación.

## 10. Estado final

La decisión registrada constituye una propuesta arquitectónica inicial. Su aceptación definitiva requiere validar los requisitos, las restricciones y los riesgos con el diagnóstico de la Actividad 1 y documentar cualquier ajuste necesario.

## 11. Referencias internas

- `01-catalogo-requisitos.md`
- `02-matriz-priorizacion.md`
- `03-escenarios-calidad.md`
- `04-comparacion-alternativas.md`
- `05-criterios-verificacion.md`