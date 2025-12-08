# Hashcat Cheat Sheet

#### Muestra las especificaciones de los dispositivos instalados de nuestro sistema e indica que OpenCL está configurado correctamente 
```
hashcat -I
```
## Ataque de Diccionario

#### Ataque por Diccionario para MD5
```
hashcat -a 0 -m 0 <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario para SHA-256 y guardar el resultado en un archivo
```
hashcat -a 0 -m 1400 -o <OUTPUT> <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario y usando rules (/usr/share/hashcat/rules/)
```
hashcat -a 0 -m 1400 -o <OUTPUT> <HASH-FILE> <WORDLIST> -r <PATH-RULE>
```

#### Ataque por Combinación de diccionarios
```
hashcat -a 1 -m 1400 -o <OUTPUT> <HASH-FILE> <WORDLIST-1> <WORDLIST-2>
```

## Ataque de Máscara

### Máscaras que se pueden usar (-m 3)
| Símbolo| Charset |
|----------|----------|
| ?l    | abcdefghijklmnoparstuvwxyz   |
| ?u    | ABCDEFGHIJKLMNOPQRSTUVWXYZ   |
| ?d    | 0123456789   |
| ?h    | 0123456789abcdef   |
| ?H    | 0123456789ABCDEF   |
| ?s    | «space»!» #$%&'()*+,-. /:;<=>? @[]^_`{   |
| ?a    | ? ¿L? ¿U? ¿D? s   |
| ?b    | 0x00 - 0xff   |

#### Ataque de máscara por Fuerza Bruta (definido por el usuario) usando 6 letras minisculas al inicio y 2 números al final
```
hashcat -a 3 -m 1400 -o <OUTPUT> <HASH-FILE> ?l?l?l?l?l?l?d?d
```

#### Ataque por Fuerza Bruta usando mascaras full de 6 digitos
```
hashcat -a 3 -m 1400 -o <OUTPUT> <HASH-FILE> ?a?a?a?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara cualquiera seguido de la palabra megatron
```
hashcat -a 3 -m 1400 -o <OUTPUT> <HASH-FILE> megatron?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara que sean 2 mayusculas, 2 minusculas, 2 números y 2 caracteres especiales
```
hashcat -a 3 -m 1400 -o <OUTPUT> <HASH-FILE> ?u?u?l?l?d?d?s?s
```

## Ataques específicos

#### Ataque por Diccionario a SSH (id_rsa) y usando rules
```
hashcat -m 22921 <HASH-FILE> <WORDLIST> -r <PATH-RULE> --force
```

#### Ataque por Diccionario a Cache dumping y usando rules
```
hashcat -m 2100 <HASH-FILE> <WORDLIST> -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a ASRepRoast y usando rules
```
hashcat -m 18200 <HASH-FILE> <WORDLIST> -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a Kerberoasting cuando el modo de hash es RC4 y usando rules
```
hashcat -m 13100 <HASH-FILE> <WORDLIST> -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a Kerberoasting cuando el modo de hash es AES256 y usando rules
```
hashcat -m 19700 <HASH-FILE> <WORDLIST> -r /usr/share/hashcat/rules/best64.rule --force
```

#### Ataque por Diccionario a NTLM
```
hashcat -m 1000 <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario a Net-NTLMv2 (Responder SMB)
```
hashcat -m 5600 <HASH-FILE> <WORDLIST>
```

#### Ataque por Diccionario a KeePass usando un Rule
```
hashcat -m 13400 <HASH-FILE> <WORDLIST> -r /usr/share/hashcat/rules/rockyou-30000.rule --force
```

#### Ataque por Diccionario a JWT usando un Rule
```
hashcat -m 16500 --force -a 0 --rules=/usr/share/hashcat/rules/InsidePro-PasswordsPro.rule token.jwt <WORDLIST>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)