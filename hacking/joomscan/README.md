# JoomScan Cheat Sheet

#### Escaneo por default
```
joomscan -u <URL>
```

#### Enumerar los componentes instalados de la victima
```
joomscan --url <URL> --enumerate-components
```

#### Establecer cookie
```
joomscan --url <URL> --cookie "test=demo;"
```

#### Especificar el uso de un User-Agent
```
joomscan --url <URL> --user-agent "Googlebot/2.1 (+http://www.googlebot.com/bot.html)"
```

#### Establecer un User-Agent random
```
joomscan --url <URL> --random-agent
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)