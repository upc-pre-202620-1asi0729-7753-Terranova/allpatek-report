# Diagramas y flujos de Allpatek

Los diagramas documentan la implementación revisada para las secciones 4.4.4 y 4.6 a 4.8.1. Distinguen la demo Angular con JSON Server/Azure Mock API, la API Java verificada por separado con MySQL, y las funciones que todavía son propuestas.

- `.puml`: fuente editable PlantUML.
- `.png`: imagen utilizada por el informe Markdown.
- `.svg`: imagen vectorial para ampliar sin perder claridad.

Generación local con Java y PlantUML 1.2026.2:

```powershell
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tpng 'assets/chapter-04/architecture/*.puml'
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tsvg 'assets/chapter-04/architecture/*.puml'
```

| Fuentes | Qué representan |
|---|---|
| 01–04 | EventStorming de la demo, contexto, contenedores y componentes de Spring |
| 05–07 | SPA Angular, landing e invocaciones a webhooks desde el navegador |
| 08–12 | Agregados, value objects, servicios y persistencia del backend |
| 13–17 | Esquema físico inspeccionado en MySQL 8.4; referencias por ID sin claves foráneas |
| 18–19 | Secuencias de la demo: acuerdos/evidencias y parcelas/clima |

**Versiones revisadas:** Webapp `f635d7f` (develop) y `33bf377` (main); landing `ccc9d71` (develop) y `35fc7c0` (main); backend `allpatek-platform.zip` (SHA-256 `333cfcbafc94fecc7d6d3df8a0ab348e272ac0be2e339fa77b0805eed0608978`). Los C4 usan la biblioteca incluida en PlantUML; la generación no requiere descargar includes.

El EventStorming describe resultados del negocio y de la UI; no acredita que Spring publique esos eventos ni reemplaza la evidencia de un taller. El PNG `05-web-components-update.png` se conserva como versión anterior de Sprint 3; la figura vigente es `05-web-components.png`.
