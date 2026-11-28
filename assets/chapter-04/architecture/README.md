# Diagramas y flujos de Allpatek

El capítulo IV del [informe](../../../README.md) explica el alquiler de una parcela por temporada, las aceptaciones y el seguimiento por hitos. Las figuras distinguen el diseño del negocio y el comportamiento presente en Angular (`996d647`), Spring (`82e8832`) y la landing (`359cf77`).

| Fuentes | Uso en el informe |
|---|---|
| `01-eventstorming`, `01a-season-agreement`, `01b-milestone-payout`, `01c-season-lifecycle` | Implementación, decisiones propuestas y relación con el Big Picture del capítulo II. |
| `02-context` y `03-containers` | Usuarios, sistemas externos, webapp y unidades desplegables. |
| `04-api-components` a `07-n8n-components` y `c4-*` | Vista general de los productos, webhooks y componentes de los siete contextos de la API y Shared. |
| `08-classes-users` a `12b-classes-alerts` y `classes-iam*`, `web-classes-*` | Clases del backend y la webapp por contexto. |
| `13-database-users` a `17-database-monitoring` y `20-database-overview`, `database-iam` | Mapeo relacional derivado de JPA y relaciones lógicas por identificador. |
| `18-flow-agreement-evidence` y `19-flow-parcels-climate` y `flow-*` | Secuencias de la demo que aparecen en 4.4.4. |

El nombre histórico `c4-shared-profiles` identifica el diagrama de Profiles. `c4-shared` cubre el soporte transversal. La [auditoría](diagram-coherence-audit.md) registra los cambios y sus fuentes.

Cada figura vigente tiene una fuente PlantUML, un PNG para el informe y un SVG para ampliar. `eventstormingudpate.png` corresponde al tablero general del capítulo II. `05-web-components-update.png` conserva una versión anterior.

Para regenerarlas con Java y PlantUML 1.2026.2 desde la raíz del informe:

```powershell
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tpng 'assets/chapter-04/architecture/*.puml'
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tsvg 'assets/chapter-04/architecture/*.puml'
```
