---
aliases:
  - Índice
tags:
  - "null"
tipo: index
---

> [!NOTE] Presentación
> Esto consiste en una prueba propia para ver de qué manera hago funcionar una pieza de Dataview basada en un índice previo

## Directorio
- - -
```dataview
LIST rows.file.link
FROM "Alberto"
WHERE file.name != this.file.name
GROUP BY file.folder
```

## Metaindex
- - -
```dataview
TABLE file.folder, tags
FROM "Alberto/1. Índices"
WHERE file.name != this.file.name
```
