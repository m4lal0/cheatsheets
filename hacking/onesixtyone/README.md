# OneSixtyOne Cheat Sheet

#### Fuerza Bruta a Community.
```
onesixtyone <COMMUNITY> <IP-Address>
onesixtyone public 192.168.4.0/24
```

#### Fuerza Bruta, obteniendo una wordlist de nombres de community y guardar el resultado.
```
onesixtyone -c <COMMUNITY-WORDLIST> <IP-ADDRESS> -o <OUTPUT-FILE>
onesixtyone -c wordlist/SecLists/Discovery/SNMP/common-snmp-community-strings-onesixtyone.txt 192.168.4.10 -o output.txt
```

#### Fuerza Bruta, obteniendo una wordlist de nombres de community, buscando en un listado de IP's guardando el resultado.
```
onesixtyone -c <COMMUNITY-WORDLIST> -i <INPUT-FILE> -o <OUTPUT-FILE>
onesixtyone -c wordlist/SecLists/Discovery/SNMP/common-snmp-community-strings-onesixtyone.txt -i host.txt -o output.txt
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)