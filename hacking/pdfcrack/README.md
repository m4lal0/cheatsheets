# PDFCrack Cheat Sheet

#### Fuerza bruta a un archivo PDF
```
pdfcrack -f <File>
```

#### Fuerza bruta a un archivo PDF usando un WordList
```
pdfcrack -f <File> -w <WORDLIST>
```

#### Fuerza bruta usando alguna palabra y números que contiene el password
```
pdfcrack -f <File> -c coche1234
```

#### Reiniciar el proceso en pausa
```
pdfcrack -f <File> -1 savedstat.sav
```

#### Fuerza bruta con un número mínimo de caracteres
```
pdfcrack -f <File> -n=12
```

#### Fuerza bruta con un número máximo de caracteres
```
pdfcrack -f <File> -m=20
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)