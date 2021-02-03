# Airmon-ng Cheat Sheet

#### Visualizar listado de interfaces en modo monitor
```
airmon-ng
```

#### Establecer tarjeta de red en modo Monitor
```
airmon-ng start <interface>
```

#### Establecer interfaz en modo monitor en un canal específico
```
airmon-ng start <interface> -c <Channel>
```

#### Eliminar procesos que pueden obstruir el uso en modo monitor
```
airmon-ng check kill
```

#### Detener el modo monitor
```
airmon-ng stop <interface>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)