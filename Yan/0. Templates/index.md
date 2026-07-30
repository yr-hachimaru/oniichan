---
aliases:
  - Índice
tags:
  - "null"
tipo: index
---

> [!NOTE] Presentación
> Contents

## Directorio
- - -
```dataview
LIST rows.file.link
FROM "Yan/0. Templates"
WHERE file.name != this.file.name
GROUP BY file.folder
```
## Referencias
- - -

```dataview
TABLE file.folder, tags
FROM [[]]
```