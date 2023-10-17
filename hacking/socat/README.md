# Socat Cheat Sheet

### Port Forwarding

#### Ejecutar en maquina local y con ello podemos acceder a 'http://localhost:8080' en la maquina atacante y obtenemos el contenido del sitio web remoto.
```
socat tcp-listen:8080,fork tcp:<TARGET-IP>:80
```

#### Ejecutar en maquina remota y con ello abrimos un el puerto SSH hacia nosotros.
```
socat tcp-listen:2222,fork tcp:<TARGET-IP>:22
```

#### Ejecutar en maquina remota y con ellos accedemos a http//<TARGET-IP>:1234 en la maquina atacante y obtener el contenido del puerto remoto 8080.
```
socat tcp-listen:1234,fork,reuseaddr tcp:localhost:8080
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)