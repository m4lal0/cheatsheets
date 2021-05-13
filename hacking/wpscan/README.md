# WPScan Cheat Sheet

#### Uso Básico
```
wpscan --url <Target> -v
```

#### Uso Básico y ocultar el banner de inicio
```
wpscan --url <Target> -v --no-banner
```

#### Escaneo Rápido
```
wpscan --url <Target> --threads 8
```

#### Guardar el resultado en un archivo
```
wpscan --url <Target> -o <FileName>
```

#### Enumerar plugins, usuarios, temas, timthumbs
```
wpscan --url <Target> --enumerate vp,u,vt,tt
```

#### Enumerar plugins usando nuestro API Token; Donde API Token lo pueden obtener desde https://wpvulndb.com/users/sign_up
```
wpscan --api-token <API-Token> --url <Target> --plugins-detection aggressive --enumerate vp
```

#### Enumerar todos los plugins
```
wpscan --url <Target> --enumerate ap
```

#### Usar un HTTP proxy
```
wpscan --url <Target> --proxy IP:PORT
```

#### Usar un SOCKS5 proxy (necesita cURL >= v7.21.7)
```
wpscan --url <Target> --proxy socks5://IP:PORT
```

#### Deshabilitar la verificación del certificado SSL/TLS 
```
wpscan --url <Target> --disable-tls-checks --enumerate vp,u -o <FileName>
```

#### Autenticación básica HTTP 
```
wpscan --url <Target> --basic-auth <Username:Password>
```

#### Fuerza Bruta para el inicio de sesión
```
wpscan --url <Target> --passwords <Wordlist-Password> --usernames <Wordlist-UserName>
```

#### Proporcionar cookie para sesiones autenticadas
```
wpscan --url <Target> --cookie <Cookie>
```

#### Escaneo Agresivo
```
wpscan --url <Target> --enumerate ap --plugins-detection mixed
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)