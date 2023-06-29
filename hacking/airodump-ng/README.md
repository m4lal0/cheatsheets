# Airodump-ng Cheat Sheet

#### Mostrar un listado de puntos de acceso wifi que detecta nuestra interfaz
```
airodump-ng <INTERFACE>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el BSSID y canal del AP.
```
airodump-ng --bssid <BSSID-AP> -c <CHANNEL-AP> <INTERFACE>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el ESSID y canal del AP.
```
airodump-ng --essid <ESSID-AP> -c <CHANNEL-AP> <INTERFACE>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el BSSID, ESSID y canal del AP.
```
airodump-ng --bssid <BSSID-AP> --essid <ESSID-AP> -c <CHANNEL-AP> <INTERFACE>
```

#### Guardar las evidencias de un punto de acceso en especifico en sus diferentes extensiones.
```
airodump-ng --bssid <BSSID-AP> --essid <ESSID-AP> -c <CHANNEL-AP> -w <OUTPUT-NAME> <INTERFACE>
```

#### Guardar las evidencias de un punto de acceso en especifico en solamente extensiones CSV y PCAP.
```
airodump-ng --bssid <BSSID-AP> --essid <ESSID-AP> -c <CHANNEL-AP> -w <OUTPUT-NAME> --output-format csv,pcap <INTERFACE>
```

#### Mostrar un listado de puntos de acceso wifi que detecta nuestra interfaz e información WPS si la hay.
```
airodump-ng -w <OUTPUT-NAME> --wps <INTERFACE>
```

#### Mostrar un listado de puntos de acceso wifi en banda 2.4GHz y 5GHz.
```
airodump-ng -w <OUTPUT-NAME> --band abg <INTERFACE>
```

#### Mostrar un listado de puntos de acceso wifi junto con su fabricante.
```
airodump-ng -w <OUTPUT-NAME> --manufacturer <INTERFACE>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)