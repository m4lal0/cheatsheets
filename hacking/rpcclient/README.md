# RPCclient Cheat Sheet

#### Acceso con Null Session
```
rpcclient -U "" <IP-TARGET> -N
```

#### Acceso con autenticación
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -N
```

#### Enumerar los Dominios
```
rpclcient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c "enumdomains"
```

#### Enumerar los usuarios del AD
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'enumdomusers'
```

#### Enumerar los grupos del AD
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'enumdomgroups'
```

#### Mostrar los datos y descripción de un usuario
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'queryuser <user>'
```

#### Enumerar los usuarios que son de un 'rid' grupo en especifico del Dominio
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'querygroupmem 0x200'
```

#### Mostrar la información de un usuario por su 'rid'
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'queryuser 0x1f4'
```

#### Mostrar la descripción de todos los usuarios
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'querydispinfo'
```

#### Crear un usuario del AD (Teniendo los privilegios necesarios)
```
rpclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET>
rpcclient> createdomuser <username>
rpcclient> setuserinfo2 <username> 24 <password>
rpcclient> enumdomusers
```

#### Eliminar un usuario del AD
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'deletedomuser <user>'
```

#### Enumerar los recursos compartidos
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'netshareenum'
```

#### Crear un Grupo de Dominio
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'createdomgroup <newgroup>'
```

#### Eliminar un Grupo de Dominio
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'deletedomgroup <group>"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)