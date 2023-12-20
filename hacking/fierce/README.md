# Fierce Cheat Sheet

#### Reconocimiento de DNS / Tranferencia de zona
```
fierce --domain <DOMAIN>
```

#### Reconocimiento de DNS y subdominios (account admin ads)
```
fierce --domain <DOMAIN> --subdomain account admin ads
```

#### Intentar una conexión HTTP en dominios descubiertos
```
fierce --domain <DOMAIN> --subdomains mail --connect
```

#### Cambia velocidad por amplitud con el indicador --wide, que busca dominios cercanos en todas las IP del /24 de un dominio descubierto
```
fierce --domain <DOMAIN> --wide
```

#### Reconocimiento de DNS a redes internas
```
fierce --dns-servers 10.0.0.1 --range 10.0.0.0/24
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)