# ARPing Cheat Sheet

#### Ping a un host
```
arping <Host/IP>
```

#### Ping a un host por su nombre
```
arping -f <Host-Name>
```

#### Ping a un host usando una interfaz, con envio de 8 solicitudes y verbose en modo detallado.
```
arping -i wlan0 -c8 <Host/IP> -vv
```

#### Dirección IP ARP caché
```
arping -U <Host/IP>
```

#### Buscar MAC duplicadas para una Ip en concreto
```
arping -D -i eth0 -c2 <Host/IP>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)