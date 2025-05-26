# RPCclient Cheat Sheet

#### Acceso con Null Session
```
rpcclient -U "" <IP-TARGET> -N
```

#### Acceso con usuario invitado
```
rpcclient -U "gest%" <IP-TARGET> -N
```

#### Acceso con autenticación
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET>
```

#### Acceso con autenticación por Hash NT
```
rpcclient -U "<USERNAME>%<NT-HASH>" <IP-TARGET> --pw-nt-hash
```

#### Password Spraying - Conocer a través de una lista de usuarios cuales tienen acceso con una contraseña dada
```
for u in $(cat valid_users.txt);do rpcclient -U "$u%<PASSWORD>" -c "getusername;quit" <IP-TARGET> | grep Authority; done
```

#### Mostrar el Dominio y su SID
```
rpclcient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c "lsaquery"
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

#### Mostrar el SID de un usuario dado
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'lookupnames <USER>'
```

#### Mostrar los datos y descripción de un usuario
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'queryuser <USER>'
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

#### Mostrar la Politica de Contraseñas
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'getdompwinfo'
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
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'deletedomuser <USER>'
```

#### Enumerar los recursos compartidos
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'netshareenum'
```

#### Crear un Grupo de Dominio
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'createdomgroup <NEW-GROUP>'
```

#### Eliminar un Grupo de Dominio
```
rpcclient -U "<USERNAME>%<PASSWORD>" <IP-TARGET> -c 'deletedomgroup <GROUP>'
```

#### Obtener el SID de un usuario que sepamos que existe
```
rpcclient -U "gest%" <IP-TARGET> -c 'lookupnames <USERNAME>'

rpcclient -U "gest%" <IP-TARGET> -c 'lookupnames Administrator'
```

#### Saber el usuario proporcionando el SID 
```
rpcclient -U "gest%" <IP-TARGET> -c 'lookupsids <SID>'
```

#### Comando para Fuerza Bruta y conocer los usuarios que existen proporcioando el SID del usuario administrator y modificar los ulitmos digitos (RPC RID Cycling Attack)
```
seq 400 2000 | xargs -P 50 -I {} rpcclient -U "gest%" <IP-TARGET> -c 'lookupsids <SID>-{}' | grep -v unknown
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)