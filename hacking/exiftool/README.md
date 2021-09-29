# Exiftool Cheat Sheet

#### Listar todos los metadatos de una imagen/archivo
```
exiftool <File-or-Image>
```

#### Exportar los metadatos a un archivo HTML
```
exiftool -h <File-or-Image> > file.html
```

#### Exportar los metadatos a formato CSV
```
exiftool -csv <File-or-Image>
```

#### Exportar los metadatos a formato JSON
```
exiftool -json <File-or-Image>
```

#### Modificar algun metadato
```
exiftool -overwrite_original <Metadata>="<String>" <File-or-Image>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)