# Android Debug Bridge (adb) Cheat Sheet


## Básicos

#### Iniciar servicio ADB
```
adb start-server
```

#### Parar servicio ADB
```
adb kill-server
```

#### Reiniciar el dispositivo
```
adb reboot
```

#### Listar dispositivos
```
adb devices
```

#### Listar dispositivos con más detalles
```
adb devices -l
```

#### Conectarnos a un dispisitivo
```
adb connect <HOST>:<PORT>
```

#### Desconectarnos de un dispisitivo
```
adb disconnect <HOST>:<PORT>
```

#### Entrar a la shell
```
add shell
```

#### Usar comando con privilegio root
```
adb shell “su -c <COMMAND> “
```

#### Conexión a la shell del dispositivo de acuerdo a su ID
```
adb -s <ID> shell
```

#### Conexión a la shell del dispositivo de acuerdo a su IP y puerto
```
adb -H <IP> -P <PORT> shell
```


## Instalación de paquetes

#### Instalar un APK al dispositivo
```
adb install <APP-NAME>
```

#### Reinstalar un APK al dispositivo
```
adb -r install <APP-NAME>
```

#### Desinstalar un APK del dispositivo
```
adb uninstall <APP-NAME>
```


## Operaciones con archivos

#### Extraer un archivo del móvil a tu máquina
```
add pull /storage/0/emulated/FILE .
```

#### Importar un archivo de tu máquina al móvil
```
add push /path/to/FILE /storage/0/emulated/
```


## Información del Móvil

#### Mostrar información sobre CPU
```
adb shell cat/proc/cpuinfo
```

#### Listar configuración de proxy del dispositivo
```
adb shell settings list global http_proxy | grep proxy
```

#### Configurar el proxy en el dispositivo
```
adb shell settings put global http_proxy 192.168.0.56:8080
```

#### Obtener el primer IMEI del dispositivo
```
adb shell "service call iphonesubinfo 1 | toybox cut -d \"'\" -f2 | toybox grep -Eo '[0-9]' | toybox xargs | toybox sed 's/\ //g'"
```

#### Obtener el segundo IMEI del dispositivo
```
adb shell "service call iphonesubinfo 3 i32 1 | toybox cut -d \"'\" -f2 | toybox grep -Eo '[0-9]' | toybox xargs | toybox sed 's/\ //g'"
```

#### Obtener el android ID en hexadecimal
```
adb shell settings get secure android_id
```

#### Mostrar el modelo del dispositivo conectado
```
adb shell getprop ro.product.model
```

#### Visualizar el estatus de la bateria del dispositivo
```
adb shell dumpsys battery
```

#### Visualizar la actividad que está actualmente en la pantalla principal del dispositivo
```
adb shell dumpsys activity activities | grep mResumedActivity
```

#### Visualizar las actividades de una aplicación
```
adb shell dumpsys activity activities | grep <PACKAGE_NAME>
```

#### Visualizar los servicios que corren de una aplicación
```
adb shell dumpsys activity services <PACKAGE_NAME>
```

#### Extraer la información acerca de una aplicación
```
adb shell dumpsys package <PACKAGE_NAME>
```


## Información de Paquetes

#### Extraer un APK del dispositivio móvil
```
add shell pm path <PACKAGE_NAME>
adb pull /data/app/<PACKAGE_NAME>/base.apk
```

#### Mostrar los paquetes que tenga instaldo el dispositivo
```
adb shell 'pm list packages -f'
adb shell 'pm list packages -f | grep PACKAGES'
```

#### Mostrar listado de todos los paquetes instadlos en el equipo
```
adb shell pm list packages
```

#### Mostrar listado de todas las apps del sistema instalados
```
adb shell pm list packages -s
```

#### Mostrar listado de todas las apps de terceros instalados
```
adb shell pm list packages -3
```

#### Listar la ruta de los archivos de una aplicación
```
adb shell pm path <PACKAGE_NAME>
```

#### Borrar la data de una aplicación
```
adb shell pm clear <PACKAGE_NAME>
```

## Logs

#### Concer el ID del proceso de una aplicación
```
adb shell pidof <PACKAGE_NAME>
```

#### Mostrar el log del dispositivo
```
adb logcat
adb logcat | grep '<SHEARCH>'
adb logcat | grep <PROCESS_ID>
adb logcat > log.txt
adb logcat -s TAG
```


## Comandos al dispositivo

#### Forward en puertos
```
adb forward tcp:<PORT> tcp:<OTHER-PORT>
```

#### Realizar un backup de una aplicación
```
add backup -apk <PACKAGE_NAME> -f backup.ab
```

#### Restaurar un backup
```
add restore backup.ab
```

#### Enviar pulsaciones de teclado al dispositivo
```
adb shell input <text|keyevent>
```

#### Iniciar un Activity
```
adb shell am start -n [PAQUETE-APLICACION]/.[ACTIVITY]
adb shell am start -n com.example.android.notepad/.NotesList


adb shell am start -a [ACTION-NAME] -n [PAQUETE-APLICACION]/.[ACTIVITY]
adb shell am start -a android.intent.action.MAIN -n com.example.android.notepad/.NotesList


adb shell am start -a [ACTION-NAME] -n [PAQUETE-APLICACION]/.[ACTIVITY] -d [SCHEMA]://[AUTHORITY]/[PATH]/[ID]
adb shell am start -a android.intent.action.EDIT -n com.example.android.notepad/.NoteEditor -d content://com.google.provider.NotePad/notes/1
```

#### Iniciar un Service para ejecutar un comando y leer el contenido de un archivo
```
adb shell am startservice -n [PAQUETE-APLICACION]/.[NAME-ACTIVITY] -e [EXTRA_KEY] [EXTRA_VALUE]

adb shell am startservice -n com.elearnsecurity.sillyservice/.SillyService -e COMMAND "'find /data/data/com.elearnsecurity.sillyservice -name private.txt -type f -exec cat {} \;'"
```TRA_VALUE]
```

#### Enviar un broadcast de un Receiver dentro de un Activity, para enviar un mensaje de texto:
```
adb shell am broadcast -a [RANDOM-NAME] -n [PAQUETE-APLICACION]/.[NAME-ACTIVITY] --es [EXTRA_KEY] [EXTRA_VALUE]
adb shell am broadcast -a EsmiBroadcast -n org.owasp.goatdroid.fourgoats/.broadcastreceivers.SendSMSNowReceiver --es phoneNumber 4321 --es message "Prueba XD"
```

#### Enviar un broadcast solamente dentro de un Receiver, para cambiar password:
```
adb shell am broadcast -a [ACTION-NAME] --es [EXTRA_KEY] [EXTRA_VALUE]
adb shell am broadcast -a com.elearnsecurity.vulnerablereceiver.CHANGEPW --es PASSWORD 1234
```

#### Mostrar info de un Query SQL (Provider)
```
adb shell content query —-uri content://com.elearnsecurity.injectme.provider.CredentialProvider/credentials

adb shell content query --uri content://com.elearnsecurity.provider.Wallet/cards -–projection name

adb shell content query --uri content://com.elearnsecurity.provider.Wallet/cards --where
"name='Bob'"
```

#### Insertar info de un query SQL
```
adb shell content insert --uri content://com.elearnsecurity.injectme.provider.CredentialProvider/credentials --bind username:s:admin3 --bind password:s:admin345
```

#### Actualizar info de un query SQL
```
adb shell content update -–uri content://com.elearnsecurity.provider.Wallet/cards --bind number:i:999999999 --where "name='Bob'"
```

#### Eliminar info de un query SQL
```
adb shell content delete --uri content://com.elearnsecurity.injectme.provider.CredentialProvider/credentials --where "id='3'"
```

## Instalación BurpSuite CA

```
curl -s http://burp/cert -x http://127.0.0.1:8080 -o cacert.der
openssl x509 -inform DER -in cacert.der -out cacert.pem
export CERT_HASH=$(openssl x509 -inform PEM -subject_hash_old -in cacert.pem | head -1)
adb root && adb remount
adb push cacert.pem "/system/etc/security/${CERT_HASH}.0"
adb shell "su -c 'chmod 644 /system/etc/security/cacerts/${CERT_HASH}.0'"
rm -rf cacert.*
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)