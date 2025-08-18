# Tinja Cheat Sheet

#### Escanear un sitio web en busqueda de SSTI por GET
```
tinja url -u "<URL>"
```

#### Escanear un sitio web en busqueda de SSTI por POST
```
tinja url -u "<URL>" -d "username=kirla"
```

#### Escanear un sitio web en busqueda de SSTI por GET y usando cookie
```
tinja url -u "<URL>" -c "<COOKIE>"
```

#### Escanear un sitio web en busqueda de SSTI por GET y usando una cabecera de autenticación
```
tinja url -u "<URL>" -H "Authentication: Bearer ey..."
```

#### Escanear en busqueda de un SSTI a un raw de Burp Suite
```
tinja raw -R <FILE-RAW>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)