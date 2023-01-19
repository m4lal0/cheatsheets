# shCheck Cheat Sheet

#### Realizar auditoria de encabezados de seguridad HTTP e informativos de un sitio web
```
shcheck <URL> -i -x
```

#### Realizar auditoria de encabezados de seguridad HTTP e informativos de un sitio web incluyendo los encabezados obsoletos
```
shcheck <URL> -i -x -k
```

#### Realizar auditoria de encabezados de seguridad HTTP a un sitio web y visualizar el resultado en un archivo JSON
```
shcheck <URL> -i -x -j
```

#### Auditoria a un sitio web con diferente puerto
```
shcheck <URL> -p <PORT> -i -x
```

#### Auditoria a varios sitios web desde un archivo
```
shcheck --hfile=<PATH_TO_FILE> -i -x
```

#### Auditoria a un sitio web colocando una cookie
```
shcheck <URL> -c <COOKIE> -i -x
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)