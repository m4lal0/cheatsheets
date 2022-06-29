# SNMPwalk command Cheat Sheet

#### Escaneo SNMP versión 2 al community public y guardar el resultado en un archivo
```
snmpwalk -v <VERSION> -c <COMMUNITY-STRING> <IP-ADDRESS>
snmpwalk -v 2c -c public 10.10.11.136 > snmpwalk.txt
```

#### Escaneo SNMP versión 1 al community public y guardar el resultado en un archivo
```
snmpwalk -v 1 -c public 10.10.11.136 > snmpwalk.txt
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)