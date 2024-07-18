# Frida Cheat Sheet

#### Listar dispositivos conectados a Frida
```
frida-ls-devices
```

#### Conectar Frida a un dispositivo en especifico.
```
frida-ps -D <ID_DEVICE>
frida-ps -H <IP:PORT>
```

#### Listar todos los procesos del dispositivo conectado por USB.
```
frida-ps -U
```

#### Listar sólo las aplicaciones que se están ejecutando.
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

#### Ejecutar una aplicación
```
frida -U -f <NAME-APP-PACKAGE>
```

#### Cargar un script externo (javascript) a una aplicación
```
frida -U -f <NAME-APP-PACKAGE> -l <NAME-SCRIPT>.js
```

---

## Scripts externos

#### Root Detection Bypass
```bash
frida -U -f <NAME-APP-PACKAGE> -l "<PATH_TO_fridantiroot.js_ON_YOUR_COMPUTER>" --no-pause

# Descargar script en: https://codeshare.frida.re/@dzonerzy/fridantiroot/
# Luego cargar el script descargado a /data/local/tmp usando adb push
```

#### SSL Pinning Bypass
```bash
frida -U -f <NAME-APP-PACKAGE> -l "<PATH_TO_fridasslpinningbypass.js_ON_YOUR_COMPUTER>" --no-pause

# Descargar script en: https://codeshare.frida.re/@pcipolloni/universal-android-ssl-pinning-bypass-with-frida/
# Luego cargar el script descargado a /data/local/tmp usando adb push
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)