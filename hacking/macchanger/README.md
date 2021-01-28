# Macchanger Cheat Sheet

#### Mostrar el listado de OUI (Organizationally Unique Identifier)
```
macchanger -l
```

#### Mostrar la dirección MAC de la tarjeta de red de una interfaz
```
macchanger -s <Interface>
```

#### Cambiar la dirección MAC a un valor específico
```
macchanger --mac=<MAC-Address> <Interface>
```

#### Crear una dirección MAC completamente aleatoria
```
macchanger -r <Interface>
```

#### Crear una dirección MAC completamente aleatoria del listado OUI
```
macchanger -a <Interface>
```

#### Crear una dirección MAC manteniendo los bytes actuales del OUI del mismo proveedor y solamente cambiar los últimos 3 pares de manera aleatoria.
```
macchanger -e <Interface>
```

#### Para devolver la dirección MAC a su valor de hardware original y permanente
```
macchanger -p <Interface>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)