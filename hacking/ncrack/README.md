# NCrack Cheat Sheet

#### Visualizar los modulos que puede usar
```
ncrack -V
```

#### Fuerza bruta con Wordlist por default a FTP
```
ncrack ftp://IP_Address
```

#### Ataque de diccionario
```
ncrack -user msfadmin -P wordlist.txt <IPAddress>
ncrack -U wordlist.txt -pass msfadmin <IPAddress>
ncrack -U wordlist.txt -P wordlist.txt <IPAddress>
```

#### Fuerza bruta con dos usuarios al servicio FTP
```
ncrack -user msfadmin,ignite -P wordlist.txt ftp://IP_Address
```

#### Restaurar ataque de fuerza bruta
```
ncrack --resume /root/.ncrack/restore.2022-01-01_01-01
```

#### Mostrar el resultado en modo listado
```
ncrack ssh://IP_Address -sL
```

#### Guardar el resultado en un archivo formato normal
```
ncrack -U wordlist.txt -P wordlist.txt <IPAddress> -oN file.txt
```

#### Guardar el resultado en un archivo formato XML
```
ncrack -U wordlist.txt -P wordlist.txt <IPAddress> -oX file.xml
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)