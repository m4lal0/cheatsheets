# Meg Cheat Sheet

#### Fuzzing web
```
meg --verbose <WORDLIST> <HOST_FILE>
```

#### Fuzzing web y guardar el resultado
```
meg --verbose <WORDLIST> <HOST_FILE> <OUTPUT>
```

#### Fuzzing web, realizando un redirect y mostrando solo resultados HTTP con código 200
```
meg --verbose --location -s 200 <WORDLIST> <HOST_FILE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)