# Crowbar Cheat Sheet

#### Ataque de fuerza bruta a RDP usando un usuario y un password
```
crowbar -b rdp -s <IP>/<CIDR> -u <USERNAME> -c <PASSWORD>
crowbar -b rdp -s 192.168.2.182/32 -u admin -c Password123
```

#### Ataque de fuerza bruta a RDP usando un diccionario de usuarios y passwords
```
crowbar -b rdp -s <IP>/<CIDR> -U <USER-LIST> -C <PASSWORD-LIST>
```

#### Ataque de fuerza bruta a RDP usando un diccionario de usuarios y passwords, guardando el resultado en un archivo
```
crowbar -b rdp -s <IP>/<CIDR> -U <USER-LIST> -C <PASSWORD-LIST> -o <OUTPUT>
```

#### Ataque de fuerza bruta a RDP usando un diccionario de usuarios y passwords
```
crowbar -b rdp -s <IP>/<CIDR> -U <USER-LIST> -C <PASSWORD-LIST>
```

#### Ataque de fuerza bruta a llave privada SSH
```
crowbar -b sshkey -s <IP>/<CIDR> -u <USER> -k /root/.ssh/id_rsa
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)