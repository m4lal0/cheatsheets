# RPCclient Cheat Sheet

#### Enumerar los usuarios del AD
```
rpcclient -U "username%password" <IP-Address> -c 'enumdomusers'
```

#### Enumerar los grupos del AD
```
rpcclient -U "username%password" <IP-Address> -c 'enumdomgroups'
```

#### Mostrar los datos y descripción de un usuario
```
rpcclient -U "username%password" <IP-Address> -c 'queryuser <user>'
```

#### Enumerar los usuarios que son de un 'rid' grupo en especifico del Dominio
```
rpcclient -U "username%password" <IP-Address> -c 'querygroupmem 0x200'
```

#### Mostrar la información de un usuario por su 'rid'
```
rpcclient -U "username%password" <IP-Address> -c 'queryuser 0x1f4'
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)