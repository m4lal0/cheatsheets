# Responder Cheat Sheet

#### Modo escucha en la interfaz eth0
```
responder -I eth0
```

#### Modo análisis a una dirección IP
```
responder -i <IP-Address> -A
```

#### Eschca en la interfazx eth0, habilitando las respuestas para consultas Netbios e iniciar el servidor proxy WPAD.
```
responder -I eth0 -rdw
```

#### Editar archivo de configuración de Responder
```
vi /usr/share/responder/Responder.conf
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)