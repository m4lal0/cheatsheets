# RPCclient Cheat Sheet

#### Acceso con Null Session
```
rpcclient -U "" <IP-Address> -N
```

#### Enumerar los Dominios
```
rpclcient -U "username%password" <IP-Address> -c "enumdomains"
```

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

#### Crear un usuario del AD (Teniendo los privilegios necesarios)
```
rpclient -U "username%password" <IP-Address>
rpcclient> createdomuser <username>
rpcclient> setuserinfo2 <username> 24 <password>
rpcclient> enumdomusers
```

#### Eliminar un usuario del AD
```
rpcclient -U "username%password" <IP-Address> -c 'deletedomuser <user>'
```

#### Enumerar los recursos compartidos
```
rpcclient -U "username%password" <IP-Address> -c 'netshareenum'
```

#### Crear un Grupo de Dominio
```
rpcclient -U "username%password" <IP-Address> -c 'createdomgroup <newgroup>'
```

#### Eliminar un Grupo de Dominio
```
rpcclient -U "username%password" <IP-Address> -c 'deletedomgroup <group>"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)