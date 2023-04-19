# MSSQLClient Cheat Sheet

#### Conexión a SQL Microsoft
```
impacket-mssqlclient <DOMAIN>/<USER-SQL>:<PASSWORD-SQL>@<IP-TARGET> -windows-auth
```

#### Conexión a SQL Microsoft en un puerto diferente
```
impacket-mssqlclient <DOMAIN>/<USER-SQL>:<PASSWORD-SQL>@<IP-TARGET> -port <PORT> -windows-auth
```

#### Conexión a SQL Microsoft usando NTHASH
```
impacket-mssqlclient <DOMAIN>/<USER-SQL>:<PASSWORD-SQL>@<IP-TARGET> -hashes ':<NTHASH>' -windows-auth
```

#### Conexión a SQL Microsoft usando autenticación Kerberos
```
impacket-mssqlclient <DOMAIN> -k
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)