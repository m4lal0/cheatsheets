# iOS Development Bridge (idb) Cheat Sheet

#### Listar dispositivos
```
idb list-targets
```

#### Listar dispositivos y mostrar el resultado en JSON
```
idb list-targets --json
```

#### Listar las aplicaciones instaladas en el equipo
```
idb list-apps --udid <UDID_DEVICE>
idb list-apps --udid 74064851-4B98-473A-8110-225202BB86F6
```

#### Listar las aplicaciones instaladas en el equipo y mostrar el resultado en JSON
```
idb list-apps --udid <UDID_DEVICE> --json
```

#### Lanzar una aplicación
```
idb launch <APP_NAME>
idb launch com.apple.mobilesafari
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)