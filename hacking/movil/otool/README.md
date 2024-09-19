# Otool Cheat Sheet

#### Búsqueda de uso de generadores numericos aleatorios inseguros en el aplicativo
```
otool -Iv <NAME-APP> | grep -w _random

otool -Iv <NAME-APP> | grep -w _srand

otool -Iv <NAME-APP> | grep -w _rand
```

#### Búsqueda de uso de algoritmos Hashing obsoletos y débiles
```
otool -Iv <NAME-APP> | grep -w _CC_MD5

otool -Iv <NAME-APP> | grep -w _CC_SHA1
```

#### Busqueda de uso de APIs inseguros
```
otool -Iv <NAME-APP> | grep -w _memcpy

otool -Iv <NAME-APP> | grep -w _strncpy

otool -Iv <NAME-APP> | grep -w _strcpy

otool -Iv <NAME-APP> | grep -w _strlen

otool -Iv <NAME-APP> | grep -w _sscanf

otool -Iv <NAME-APP> | grep -w _printf

otool -Iv <NAME-APP> | grep -w _fopen
```

#### Revisar si la aplicación binaria esta cifrada o no (si cryptid es 0 es vulnerable)
```
otool -l <NAME-APP> | grep -A4 LC_ENCRYPTION_INFO
```

#### Aplicación compilada sin bandera fPIE-pie (Si reporta la palabra 'PIE' no es vulnerable)
```
otool -Vh <NAME-APP>
```

#### Aplicación compilada sin bandera fobjc-arc (Si no reporta nada es vulnerable)
```
otool -Iv <NAME-APP> | grep -w _objc_release
```

#### Aplicación compilada sin bandera fstack-protector-all (Si no reporta nada es vulnerable)
```
otool -Iv <NAME-APP> | grep -w ___stack_chk_guard
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)