# Airodump-ng Cheat Sheet

#### Mostrar un listado de puntos de acceso wifi que detecta nuestra interfaz
```
airodump-ng <Interface>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el BSSID y canal del AP.
```
airodump-ng --bssid <BSSID-AP> -c <Channel-AP> <Interface>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el ESSID y canal del AP.
```
airodump-ng --essid <ESSID-AP> -c <Channel-AP> <Interface>
```

#### Mostrar un punto de acceso especifico y sus clientes conectado (si los hay); con tener el BSSID, ESSID y canal del AP.
```
airodump-ng --bssid <BSSID-AP> --essid <ESSID-AP> -c <Channel-AP> <Interface>
```

#### Guardar las evidencias de un punto de acceso en especifico en un archivo CSV.
```
airodump-ng --bssid <BSSID-AP> --essid <ESSID-AP> -c <Channel-AP> -w <FileName> <Interface>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)