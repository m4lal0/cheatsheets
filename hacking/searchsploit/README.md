# Searchsploit Cheat Sheet

#### Actualizar la BD de exploits
```
searchsploit -u
```

#### Buscar vulnerabilidades de una aplicación
```
searchsploit <NombreAlicacion>
```

#### Mostrar de que trata, la URL y el Path del exploit
```
searchsploit -p <ID>
```

#### Mostrar el script del exploit
```
searchsploit -x <ID>
```

#### Copiar el fichero en el directorio en el que estamos
```
searchsploit -m <ID>
```

#### Mostrar la URL del exploit ligado a la web exploit-db
```
searchsploit -w <NombreAlicacion>
```

#### Mostrar el resultado en formato JSON y comprobar todos los resultados de los servicios de un XML de NMAP
```
searchsploit -j --nmap <NmapFile.xml>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)