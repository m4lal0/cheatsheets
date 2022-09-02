# cURL Cheat Sheet

#### GET HTTP
```
curl -v -X GET <URL>
```

#### POST HTTP
```
curl -v -X POST --data "<DATA>" <URL>
curl -v -X POST --data "msg=whoami" <URL>
```

#### Modo silencioso
```
curl -s <URL>
```

#### Guardar la salida en un archivo
```
curl <URL> -o <FILE>
```

#### Mostrar los Headers
```
curl -I <URL>
```

#### Realizar redirecciones
```
curl -L <URL>
```

#### Autenticación básica
```
curl --user <USERNAME>:<PASSWORD> <URL>

ó

curl -u <USERNAME>:<PASSWORD> <URL>
```

#### Usar Encabezados personalizados
```
curl -H 'user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/80.0.3987.163 Safari/537.36' <URL>
```

#### Modificar User-Agent
```
curl -A 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10.12; rv:55.0) Gecko/20100101 Firefox/55.0' <URL>
```

#### Enviar un cookie
```
curl -v --cookie "NAME_COOKIE=VALUE_COOKIE" <URL>
```

#### Permitir conexiones de servidor inseguras cuando se usa SSL
```
curl -k <URL-with-HTTPS>

ó

curl --insecure <URL-with-HTTPS>
```

#### Obtener el código HTTP de respuesta de un sitio
```
curl --write-out "%{http_code}\n" -o /dev/null -s <URL>
```

#### Obtener el código HTTP de respuesta de un sitio con HTTPS
```
curl --write-out "%{http_code}\n" -o /dev/null --insecure <URL-with-HTTPS>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)