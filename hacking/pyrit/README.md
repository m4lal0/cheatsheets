# Pyrit Cheat Sheet

#### Análisis de captura
```
pyrit -r <File.cap> analyze
```

#### Cracking Password sabiendo el ESSID del AP
```
pyrit -e <ESSID> -i <Wordlist> -r <File.cap> attack_passthrough
```

#### Cracking Password sabiendo el BSSID del AP
```
pyrit -b <BSSID> -i <Wordlist> -r <File.cap> attack_passthrough
```

#### Cracking Password frente a Rainbow Table
```
pyrit -i <File.genpmk> -e <ESSID> -r <File.cap> attack_cowpatty
```
---
### Cracking a través de ataque por Base de Datos:

#### Importar contraseñar de nuestro diccionario a la BD de Pyrit
```
pyrit -i <Wordlist> import_passwords
```

#### Especificar el ESSID a trabajar
```
pyrit -e <ESSID> create_essid
```

#### Generar claves precomputadas
```
pyrit batch
```

#### Cracking Password usando la BD de Pyrit
```
pyrit -r <File.cap> attack_db
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)