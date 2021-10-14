# Hashcat Cheat Sheet

#### Ataque por Diccionario para MD5
```
hashcat -a 0 -m 0 <Hash-File> <Wordlist>
```

#### Ataque por Diccionario para SHA-256 y guardar el resultado en un archivo
```
hashcat -a 0 -m 1400 -o <Output> <Hash-File> <Wordlist>
```

#### Ataque por Diccionario y usando rules
```
hashcat -a 0 -m 1400 -o <Output> <Hash-File> <Wordlist> -r <Path-Rule>
```

#### Ataque por Combinación de diccionarios
```
hashcat -a 1 -m 1400 -o <Output> <Hash-File> <Wordlist-1> <Wordlist-2>
```

#### Ataque por Fuerza Bruta usando mascaras de 6 letras minisculas al inicio y 2 números al final
```
hashcat -a 3 -m 1400 -o <Output> <Hash-File> ?l?l?l?l?l?l?d?d
```

#### Ataque por Fuerza Bruta usando mascaras full de 6 digitos
```
hashcat -a 3 -m 1400 -o <Output> <Hash-File> ?a?a?a?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara cualquiera seguido de la palabra megatron
```
hashcat -a 3 -m 1400 -o <Output> <Hash-File> megatron?a?a?a
```

#### Ataque por Fuerza Bruta usando una mascara que sean 2 mayusculas, 2 minusculas, 2 números y 2 caracteres especiales
```
hashcat -a 3 -m 1400 -o <Output> <Hash-File> ?u?u?l?l?d?d?s?s
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)