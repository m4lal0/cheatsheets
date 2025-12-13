# JWT_Tool Cheat Sheet

#### Verificar token
```
python3 jwt_tool.py <JWT-TOKEN>
```

#### Modificar valores (Tampering)
```
python3 jwt_tool.py <JWT-TOKEN> -T
```

#### Cracking a secret key
```
python3 jwt_tool.py <JWT-TOKEN> -C -d <WORDLIST>
```

#### None algorithm Attack
```
python3 jwt_tool.py <JWT-TOKEN> -X a
```

#### Key confusion Attack
```
python3 jwt_tool.py <JWT-TOKEN> -X k -pk <PUBKEY.PEM>
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)