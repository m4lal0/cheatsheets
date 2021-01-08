# Crunch Cheat Sheet

### Crear una Wordlist de 1 a 2 dígitos de longitud de puros números
```
crunch 1 2 0123456789 -o <FileName>
```

### Crear una Wordlist de 2 a 5 dígitos de longitud mezclando números y letras
```
crunch 2 5 asdf12345 -o <FileName>
```

### Crear una Wordlist donde el objetivo elegido usa la palabra 'pass' más 2 dígitos para sus contraseñas
```
crunch 6 6 -t pass%% -o <FileName>
```

### Crear una Wordlist indicando que las combinaciones van a ser la palabra 'pass' más 1 número, una letra minúscula, una mayúscula y un símbolo
```
crunch 8 8 -t pass%@,^ -o <FileName>
```

### Crear una Wordlist usando el archivo charset Rainbow
```
crunch 2 3 /usr/share/rainbowcrack/charset.txt -o <FileName>
```

### Generar una combinación de palabras
```
crunch 1 10 -p Hello m4lal0 Users
```