# Hashcat Cheat Sheet

#### Ataque por Diccionario para MD5
```
hashcat -a 0 -m 0 <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario para SHA-256 y guardar el resultado en un archivo
```
hashcat -a 0 -m 1400 -o <Output> <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario y usando rules
```
hashcat -a 0 -m 1400 -o <Output> <HASH-FILE> <WORDLIST> -r <PATH-RULE>
```

#### Ataque por Combinación de diccionarios
```
hashcat -a 1 -m 1400 -o <Output> <HASH-FILE> <WORDLIST-1> <WORDLIST-2>
```

#### Ataque por Fuerza Bruta usando mascaras de 6 letras minisculas al inicio y 2 números al final
```
hashcat -a 3 -m 1400 -o <Output> <HASH-FILE> ?l?l?l?l?l?l?d?d
```

#### Ataque por Fuerza Bruta usando mascaras full de 6 digitos
```
hashcat -a 3 -m 1400 -o <Output> <HASH-FILE> ?a?a?a?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara cualquiera seguido de la palabra megatron
```
hashcat -a 3 -m 1400 -o <Output> <HASH-FILE> megatron?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara que sean 2 mayusculas, 2 minusculas, 2 números y 2 caracteres especiales
```
hashcat -a 3 -m 1400 -o <Output> <HASH-FILE> ?u?u?l?l?d?d?s?s
```

#### Ataque por Diccionario a SSH (id_rsa) y usando rules
```
hashcat -m 22921 <HASH-FILE> <WORDLIST> -r <PATH-RULE> --force
```

#### Ataque por Diccionario a Cache dumping y usando rules
```
hashcat -m 2100 <HASH-FILE> /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a ASRepRoast y usando rules
```
hashcat -m 18200 <HASH-FILE> /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a Kerberoasting y usando rules
```
hashcat -m 13100 <HASH-FILE> /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a NTLM
```
hashcat -m 1000 <HASH-FILE> rockyou.txt
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)