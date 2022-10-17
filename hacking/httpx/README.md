# httpx Cheat Sheet

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta
```
httpx -silent -probe -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y guardar el resultado en un archivo
```
httpx -silent -probe -list <HOST.txt> -o <OUTPUT>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y guardar el resultado en un archivo JSON
```
httpx -silent -probe -list <HOST.txt> -json <OUTPUT>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el código HTTP de respuesta, el titulo del sitio y redirecciñon
```
httpx -status-code -title -location -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y el nombre del servidor
```
httpx -silent -probe -server -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y mostrar las tecnologias que usa
```
httpx -silent -probe -tech-detect -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y mostrar la IP
```
httpx -silent -probe -ip -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y mostrar solo los que respondan con código 503 HTTP
```
httpx -silent -probe -mc 503 -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y no mostrar los que respondan con código 404 y 503 HTTP
```
httpx -silent -probe -fc 404,503 -list <HOST.txt>
```

#### Ejecutar la herramienta contra un listado de host, mostrando el estado de respuesta y probar cada URL tanto en HTTP como en HTTPS
```
httpx -silent -probe -nf -list <HOST.txt>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)