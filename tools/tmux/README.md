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
| <kbd>prefix</kbd>      | Ctrl + b       |
| <kbd>prefix</kbd> + <kbd>c</kbd>      | Crea una nueva pestaña de trabajo       |
| <kbd>prefix</kbd> + <kbd>,</kbd>      | Renombrar la pestaña de trabajo       |
| <kbd>prefix</kbd> + <kbd>-</kbd>      | Coloca un panel horizontal       |
| <kbd>prefix</kbd> + <kbd>_</kbd>      | Coloca un panel vertical       |
| <kbd>prefix</kbd> + <kbd>x</kbd>      | Elimina la pestaña donde estamos situados       |
| <kbd>prefix</kbd> + <kbd>h</kbd>      | Moverse al panel de la izquierda       |
| <kbd>prefix</kbd> + <kbd>j</kbd>      | Moverse al panel de arriba       |
| <kbd>prefix</kbd> + <kbd>k</kbd>      | Moverse al panel de abajo       |
| <kbd>prefix</kbd> + <kbd>l</kbd>      | Moverse al panel de la derecha       |
| <kbd>prefix</kbd> + <kbd>space</kbd>      | Rota el panel de vertical a horizontal ó al reves       |
| <kbd>prefix</kbd> + <kbd>{</kbd>      | Mueve lo del panel de la derecha a la izquierda       |
| <kbd>prefix</kbd> + <kbd>}</kbd>      | Mueve lo del panel de la izquierda a la derecha       |
| <kbd>prefix</kbd> + <kbd>H</kbd>      | Redimensionar el panel a la izquierda       |
| <kbd>prefix</kbd> + <kbd>K</kbd>      | Redimensionar el panel para arriba       |
| <kbd>prefix</kbd> + <kbd>J</kbd>      | Redimensionar el panel para abajo       |
| <kbd>prefix</kbd> + <kbd>L</kbd>      | Redimensionar el panel a la derecha       |
| <kbd>prefix</kbd> + <kbd>!</kbd>      | Manda el contenido de un panel a una pestaña nueva       |
| <kbd>prefix</kbd> + <kbd>t</kbd>      | Nos muestra la hora actual       |
| <kbd>prefix</kbd> + <kbd>m</kbd>      | Habilita/Deshabilita el mouse       |
| <kbd>prefix</kbd> + <kbd>d</kbd>      | Desconectar sesión y dejarla en segundo plano       |

### Enviar un shell-command
```
tmux -c "<comando>"
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)