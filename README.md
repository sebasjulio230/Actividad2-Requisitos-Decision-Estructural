# Actividad 2. Requisitos y decisión estructural

## 1. Descripción del proyecto

Esta actividad tiene como propósito analizar los requisitos de una plataforma logística y establecer una decisión arquitectónica inicial que responda a las necesidades del negocio. Se busca definir las funcionalidades principales, priorizar los requisitos, establecer atributos de calidad y comparar alternativas estructurales teniendo en cuenta sus beneficios, costos, riesgos y complejidad.

## 2. Objetivo

Definir y priorizar los requisitos funcionales y los atributos de calidad de la plataforma logística, comparar alternativas de arquitectura y justificar una decisión estructural coherente con las necesidades del negocio.

## 3. Alcance

El análisis contempla la identificación de requisitos, la priorización de necesidades, la definición de escenarios de calidad medibles, la comparación de alternativas arquitectónicas y la documentación de la decisión mediante un registro de decisión arquitectónica (ADR).

## 4. Requisitos prioritarios

Los requisitos se organizarán según su importancia para el negocio, su impacto arquitectónico y su complejidad. Se tendrán en cuenta las funcionalidades relacionadas con la gestión logística, así como los atributos de rendimiento, seguridad, disponibilidad, mantenibilidad y capacidad de evolución.

El detalle de los requisitos y su priorización se encuentra en la carpeta `docs/actividad-2/`.

## 5. Alternativas arquitectónicas

Se evaluarán dos alternativas principales:

- **Monolito modular:** una aplicación organizada en módulos con responsabilidades y límites claramente definidos.
- **Arquitectura distribuida por servicios:** una solución compuesta por servicios independientes que se comunican mediante interfaces definidas.

La evaluación considerará el costo, la complejidad, la velocidad de implementación, la facilidad de evolución, el riesgo operativo y la alineación con las necesidades del negocio.

## 6. Decisión arquitectónica

La decisión se documentará en el archivo `ADR-001-decision-arquitectonica.md`, después de comparar las alternativas y relacionarlas con los requisitos identificados para la plataforma logística.

## 7. Documentación

La documentación de la actividad estará organizada de la siguiente manera:

- `01-catalogo-requisitos.md`: catálogo de requisitos funcionales y atributos de calidad.
- `02-matriz-priorizacion.md`: matriz de priorización de requisitos.
- `03-escenarios-calidad.md`: escenarios de calidad con métricas verificables.
- `04-comparacion-alternativas.md`: comparación de las alternativas arquitectónicas.
- `05-criterios-verificacion.md`: criterios para comprobar el cumplimiento de los requisitos.
- `ADR-001-decision-arquitectonica.md`: registro de la decisión arquitectónica.

## 8. Verificación

La propuesta arquitectónica se revisará mediante criterios verificables relacionados con el cumplimiento de los requisitos, el rendimiento, la seguridad, la disponibilidad y la facilidad de mantenimiento y evolución.

## 9. Control de versiones

El trabajo se gestionará mediante Git y se publicará en un repositorio de GitHub, utilizando commits que permitan evidenciar la evolución de la documentación y las decisiones tomadas.