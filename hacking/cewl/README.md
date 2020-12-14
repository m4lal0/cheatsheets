# cewl Cheat Sheet

### Rastrear un sitio y escribir todas las palabras encontradas en un archivo

- `cewl -w <file> <url>`

### Rastrear un sitio y seguir enlaces a otros sitios

- `cewl -o <url>`

### Spider a un sitio usando un user-agent determinado

- `cewl -u <user-agent> <url>`

### Crear un archivo de palabras de un sitio con una profundidad determinada y una longitud mínima de palabras

- `cewl -w <file> -d <depth> -m <min-word-length> <url>`

### Spider a un sitio e incluir un recuento de cada palabra

- `cewl -c <url>`

### Spider a un sitio que incluya metadatos y separar las palabras de meta_datos

- `cewl -a -meta_file <file> <url>`

### Spider a un sitio y almacenar direcciones de correo electronico en un archivo separado

- `cewl -e -email_file <file> <url>`