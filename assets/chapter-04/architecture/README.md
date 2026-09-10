# Diagramas de arquitectura de Allpatek

Esta versión reemplaza la primera propuesta técnica. Los diagramas siguen los módulos descritos en las secciones 4.6 a 4.8.1.

- `.puml`: fuente editable PlantUML.
- `.png`: imagen utilizada por el informe Markdown.
- `.svg`: imagen vectorial para ampliar sin perder claridad.

Generación local con Java y PlantUML 1.2026.2:

```powershell
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tpng 'assets/chapter-04/architecture/*.puml'
java '-Djava.awt.headless=true' -jar '<ruta-plantuml.jar>' -charset UTF-8 -tsvg 'assets/chapter-04/architecture/*.puml'
```

El diseño de datos no es una base de datos implementada. El taller de EventStorming debe documentarse con evidencias reales cuando se realice.
