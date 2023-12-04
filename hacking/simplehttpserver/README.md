# SimpleHTTPServer Cheat Sheet

#### Crear webserver en el directorio de trabajo actual y en un puerto especifico
```
simplehttpserver -listen 127.0.0.1:<PORT>
```

#### Crear webserver en un directorio dado y en un puerto especifico
```
simplehttpserver -listen 127.0.0.1:<PORT> -path </DIRECTORY/>
```

#### Crear webserver en un directorio dado, en un puerto especifico y habilitando la carga de archivos
```
simplehttpserver -listen 127.0.0.1:<PORT> -path </DIRECTORY/> -upload
```

#### Crear webserver en un directorio dado, en un puerto especifico, habilitando la carga de archivos y colocar un máximo de tamaño de carga (default 50 MB)
```
simplehttpserver -listen 127.0.0.1:<PORT> -path </DIRECTORY/> -upload -max-file-size 100
```

#### Crear webserver en un directorio dado, en un puerto especifico y habilitando HTTPS
```
simplehttpserver -listen 127.0.0.1:<PORT> -path </DIRECTORY/> -https
```

#### Crear webserver en un directorio dado, en un puerto especifico e implementando una autenticación básica
```
simplehttpserver -listen 127.0.0.1:<PORT> -path </DIRECTORY/> -basic-auth <USER>:<PASSWORD>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)