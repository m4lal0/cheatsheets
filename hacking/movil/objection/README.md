# Objection Cheat Sheet

#### Conexión.
```
objection -g <PACKAGE_NAME> explore
```

#### Listar el entorno.
```
env
```

#### Información de Frida.
```
frida
```

#### Cargar archivo.
```
file upload <LOCAL_PATH> <REMOTE_PATH>
```

#### Descargar archivo.
```
file download <REMOTE_PATH> <LOCAL_PATH> 
```

#### Importar script Frida.
```
import <LOCAL_PATH_FRIDA_SCRIPT>
```

#### SSLPinning.
```
android sslpinning disable
```

#### Deshabilitar Root detection.
```
android root disable
```

#### Simular un entorno de Android Rooteado.
```
android root simulate
```

#### Ejecutar comando.
```
android shell_exec <COMMAND>
```

#### Screenshots.
```
android ui screenshot /tmp/screenshot
```

#### Habilitar captura de pantalla.
```
android ui FLAG_SECURE false
```

#### Listar activities, receivers y services.
```
android hooking list activities
android hooking list receivers
android hooking list services
```

#### Obtener activity actual.
```
android hooking get current_activity
```

#### Buscar classes dentro de nuestra aplicación.
```
android hooking search classes <PACKAGE_NAME>
```

#### Buscar metodos dentro de una classes de nuestra aplicación.
```
android hooking search methods <PACKAGE_NAME> <CLASSES_NAME>
```

#### Conectarse a una BD.
```
sqlite connect <BD_PATH>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)