# SSHuttle Cheat Sheet

#### Reenviar tráfico a través del pivote
```
sshuttle -r <USER>@<IP-PIVOTING-MACHINE> x.x.x.x/24

sshuttle -r test@<192.168.1.80 192.168.2.0/24
```

#### Excluir alguna red para no ser transmitida por el túnel
```
sshuttle -vNr <USER>@<IP-PIVOTING-MACHINE> -x x.x.x.x.x/24
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)