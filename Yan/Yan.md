
> [!NOTE] Introducción
> Esta es mi página de presentación. Al llevar mi nombre, facilita que me menciones en tu base. De esta manera, la presente página sirve de "estación de tren" a través de la cual generas rutas de información hacia temas concretos.
> 
## Índice de notas
- - -
```dataview
LIST rows.file.link
FROM "Yan" 
WHERE file.name != this.file.name AND file.folder != "Yan/0. Templates"
GROUP BY file.folder

```
- - -