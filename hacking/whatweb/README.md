# Whatweb Cheat Sheet

#### Identificar técnologias de un sitio web
```
whatweb <URL>
```

#### Identificar técnologias de un sitio web con más detalle
```
whatweb <URL> -v
```

#### Escaneo agresivo
```
whatweb -a 3 <URL>
```

#### Guardar el resultado en un archivo
```
whatweb --log-verbose=<NameFile> <URL>
```

#### Escaneo agresivo y seleccionar el plugin a buscar
```
whatweb -p <PluginName> -a 3 <URL>
```

#### Escaneo a traves de un archivo con listado de URL´s
```
whatweb -i <ListName>
```

#### Ver listado de plugins soportados
```
whatweb -l
```

#### Buscar un plugin en especifico
```
whatweb -I=<PluginName>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)