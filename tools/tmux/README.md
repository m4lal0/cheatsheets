# Tmux Cheat Sheet

### Lanzar tmux y darle un nombre al área de trabajo
```
tmux new -s <My_Session>
```

### Listar las sesiones que estan corriendo
```
tmux ls
```

### Volver a conectarse a una sesión
```
tmux attach-session -t <My_Session>
```

### Atajos de teclado

| Comando| Uso                    |
| ------------- | ------------------------------ |
| prefix      | Ctrl + b       |
| `prefix + c`      | Crea una nueva pestaña de trabajo       |
| `prefix + ,`      | Renombrar la pestaña de trabajo       |
| `prefix + -`      | Coloca un panel horizontal       |
| `prefix + _`      | Coloca un panel vertical       |
| `prefix + x`      | Elimina la pestaña donde estamos situados       |
| `prefix + h`      | Moverse al panel de la izquierda       |
| `prefix + j`      | Moverse al panel de arriba       |
| `prefix + k`      | Moverse al panel de abajo       |
| `prefix + l`      | Moverse al panel de la derecha       |
| `prefix + space`      | Rota el panel de vertical a horizontal ó al reves       |
| `prefix + {`      | Mueve lo del panel de la derecha a la izquierda       |
| `prefix + }`      | Mueve lo del panel de la izquierda a la derecha       |
| `prefix + H`      | Redimensionar el panel a la izquierda       |
| `prefix + K`      | Redimensionar el panel para arriba       |
| `prefix + J`      | Redimensionar el panel para abajo       |
| `prefix + L`      | Redimensionar el panel a la derecha       |
| `prefix + !`      | Manda el contenido de un panel a una pestaña nueva       |
| `prefix + t`      | Nos muestra la hora actual       |
| `prefix + m`      | Habilita/Deshabilita el mouse       |
| `prefix + d`      | Desconectar sesión y dejarla en segundo plano       |

### Enviar un shell-command
```
tmux -c "<comando>"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)