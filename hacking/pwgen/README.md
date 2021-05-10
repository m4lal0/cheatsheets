# pwgen Cheat Sheet

#### Generar 160 password con 8 caracteres de longitud
```
pwgen
```

#### Generar 160 password seguros con 8 caracteres
```
pwgen -s
```

#### Generar un solo password seguro de 8 caracteres
```
pwgen -s -1
```

#### Generar un solo password seguro de 14 caracteres
```
pwgen -s 14 1
```

#### Generar 2 password seguros aleatorios de 18 caracteres
```
pwgen -s 18 2
```

#### Generar un password seguro y no incluir numeros con 10 caracteres
```
pwgen -s -0 10 1
```

#### Generar un password seguro usando symbolos y caracteres especiales con longitud de 12
```
pwgen -sy 12 1
```

#### Generar un password seguro usando symbolos, con caracteres especiales y no incluir caracteres ambiguos, con longitud de 10
```
pwgen -Bsy 10 1
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)