# ldeep Cheat Sheet

#### Obtener los usuarios del dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' users
```

#### Obtener los usuarios del dominio y guardarlo en un archivo
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -o <OUTPUT> users
```

#### Obtener los usuarios con autenticación previa de Kerberos desactivada (AS-REP Roasting vulnerable)
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' users nokrbpreauth
```

#### Obtener los SPNs (Kerberoasting vulnerable)
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' users spn
```

#### Obtener cuentas con LAPS (Local Administrator Password Solutions)
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' laps
```

#### Obtener los GPO del dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' gpo
```

#### Obtener las computadoras del dominio y guardarlo en un archivo
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' -o <OUTPUT> computers
```

#### Obtener los grupos
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' groups
```

#### Obtener las cuentas de equipos
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' machines
```

#### Obtener las OUs (Organizational Units)
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' ou
```

#### Obtener las delegaciones
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' delegations
```

#### Obtener las politicas del Dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' domain_policy
```

#### Obtener los roles FSMO
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' fsmo
```

#### Obtener las cuentas de servicio administradas por el grupo gMSA del dominio
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' gmsa
```

#### Obtener los Servicios de certificados del directorio activo (ADCS)
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' pkis
```

#### Obtener más información sobre la plantilla de certificado
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' templates
```

#### Obtener los grupos que pertenece un usuario en especifico
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' memberships <USER> -r
```

#### Obtener los grupos que sean Domain Admins
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' membersof 'domain admins'
```

#### Obtener credenciales si se almacenan de forma insegura en LDAP de un usuario
```
ldeep ldap -d <DOMAIN> -s <IP-TARGET> -u '<USER>' -p '<PASSWORD>' search '(samaccountname=<USER>)' userPassword
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)