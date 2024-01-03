# WPScan Cheat Sheet

#### Uso Básico
```
wpscan --url <URL-TARGET> -v
```

#### Uso Básico y ocultar el banner de inicio
```
wpscan --url <URL-TARGET> -v --no-banner
```

#### Escaneo Rápido
```
wpscan --url <URL-TARGET> --threads 8
```

#### Guardar el resultado en un archivo
```
wpscan --url <URL-TARGET> -o <FILE-NAME>
```

#### Enumerar plugins, usuarios, temas, timthumbs
```
wpscan --url <URL-TARGET> --enumerate vp,u,vt,tt
```

#### Enumerar plugins usando nuestro API Token; Donde API Token lo pueden obtener desde https://wpvulndb.com/users/sign_up
```
wpscan --api-token <API-TOKEN> --url <URL-TARGET> --plugins-detection aggressive --enumerate vp
```

#### Enumerar todos los plugins
```
wpscan --url <URL-TARGET> --enumerate ap
```

#### Usar User-Agent random
```
wpscan --url <URL-TARGET> --rua
```

#### Usar un HTTP proxy
```
wpscan --url <URL-TARGET> --proxy IP:PORT
```

#### Usar un SOCKS5 proxy (necesita cURL >= v7.21.7)
```
wpscan --url <URL-TARGET> --proxy socks5://IP:PORT
```

#### Deshabilitar la verificación del certificado SSL/TLS 
```
wpscan --url <URL-TARGET> --disable-tls-checks --enumerate vp,u -o <FILE-NAME>
```

#### Autenticación básica HTTP 
```
wpscan --url <URL-TARGET> --basic-auth <Username:Password>
```

#### Password Spraying a un usuario
```
wpscan --url <URL-TARGET> -P <WORDLIST-PASSWORD>
```

#### Fuerza Bruta para el inicio de sesión
```
wpscan --url <URL-TARGET> --passwords <WORDLIST-PASSWORD> --usernames <WORDLIST-USERNAME>
```

#### Proporcionar cookie para sesiones autenticadas
```
wpscan --url <URL-TARGET> --cookie <COOKIE>
```

#### Escaneo Agresivo
```
wpscan --url <URL-TARGET> --enumerate ap --plugins-detection mixed
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)