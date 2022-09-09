# Frida-ps Cheat Sheet

#### Conectar Frida a un dispositivo en especifico.
```
frida-ps -D <ID_DEVICE>
frida-ps -H <IP:PORT>
```

#### Listar todos los procesos del dispositivo conectado por USB.
```
frida-ps -U
```

#### Listar aplicaciones corriendo.
```
frida-ps -Ua
```

#### Listar aplicaciones instaladas.
```
frida-ps -Uai
```

#### Listar aplicaciones instaladas y guardar los resultados en un JSON.
```
frida-ps -Uaij -O <OUTPUT>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)