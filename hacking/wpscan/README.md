# WPScan Cheat Sheet

#### Uso Básico
```
wpscan --url <target> -v
```

#### Guardar el resultado en un archivo
```
wpscan --url <target> -o <fileName>
```

#### Enumerar plugins, usuarios, temas, timthumbs
```
wpscan --url <target> --enumerate vp,u,vt,tt
```

#### Enumerar todos los plugins
```
wpscan --url <target> --enumerate ap
```

#### Usar un HTTP proxy
```
wpscan --url <target> --proxy IP:PORT
```

#### Usar un SOCKS5 proxy (necesita cURL >= v7.21.7)
```
wpscan --url <target> --proxy socks5://IP:PORT
```

#### Deshabilitar la verificación del certificado SSL/TLS; Donde TOKEN lo pueden obtener desde https://wpvulndb.com/users/sign_up 
```
wpscan --url <target> --disable-tls-checks --enumerate vp,u -o <fileName>
```

#### Escaneo Agresivo
```
wpscan --url <target> --enumerate ap --plugins-detection mixed
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)