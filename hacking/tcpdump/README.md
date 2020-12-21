# TCPdump Cheat Sheet

### Listas interfaces de red del sistema

+ `tcpdump -D`

### Capturar paquetes y guardarlo en un archivo

+ `tcpdump -i eth0 -w filename.cap -v`

### Captura de paquetes con salida más detallada

+ `tcpdump -i eth0 -nnvvS`

### Leer los paquetes de un archivo

+ `tcpdump -tttt -r filename.cap`

### Muestra direcciones IP en lugar de nombres de host al capturar paquetes

+ `tcpdump -i eth0 -n`

### Muestra los paquetes capturados en formato HEX y ASCII

+ `tcpdump -i eth0 -XX`

### Capturar paquetes de una dirección IP de origen / destino en particular

+ `tcpdump src 192.168.1.1`
+ `tcpdump dst 192.168.1.1`

### Capturar paquetes de un número de puerto de origen / destino en particular

+ `tcpdump src port 53`
+ `tcpdump dst port 21`

### Capture el tráfico de una red completa utilizando la notación CIDR

+ `tcpdump net 192.168.1.0/24`

### Capture el tráfico hacia o desde un puerto

+ `tcpdump port 3389`

### Muestra los paquetes capturados por encima o por debajo de un cierto tamaño (en bytes)

+ `tcpdump less 64`
+ `tcpdump greater 256`