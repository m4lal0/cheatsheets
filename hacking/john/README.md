# John the Ripper Cheat Sheet

### Mostrar los tipos de contraseñas que John puede decifrar con la velocidad del crack (crack/segundo)

- `john --test`

## Modos de Cracking

### Para usar una lista de palabras

- `john --worlist=<Wordlist> <PasswordFile>`

### Modo incremental (Brute Force)

- `john --incremental <hashfile>`

### Forzar hash a un tipo de formato (Ejemplo formato NT)

- `john --format=NT <hashfile>`

### Mostrar resultados después de ejecutar John

- `john --show`

## Sesión y Restauración

### Restaurar una sesión de John interrumpida

- `john --restore:<name>`