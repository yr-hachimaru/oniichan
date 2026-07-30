## Conexiones
- - -
```dataview
TABLE file.folder, tags
FROM [[]]
```
- - -
## Metaindex
- - -
```dataview
TABLE file.folder, tags
FROM "Yan/1. Index"
WHERE file.name != this.file.name
```
