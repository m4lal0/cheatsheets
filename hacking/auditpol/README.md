# Auditpol Cheat Sheet

Comando | Descripción
-- |  --
`/set` | Establece la política de auditoría.
`/get` | Muestra la política de auditoría actual.
`/backup` | Guardar la política de auditoría en un archivo.
`/list` | Mostrar los elementos seleccionables de la política de auditoría.
`/restore` | Restaura la política de auditoría a partir de un archivo creado previamente mediante auditpol/backup.
`/remove` | Elimina todos los ajustes de la política de auditoría del sistema.
`/clear` | Borrar la política de auditoría.
`/resourceSACL` | Configura las listas de control de acceso de recursos globales (SALCs).

### Visualizar todas las Políticas de auditoría
```
auditpol /get /category:*
```

### Habilitar Política de auditoría
```
auditpol /set /category:"system","account logon" /success:enable /failure:enable
```

### Limpiar Políticas de auditoría
```
auditpol /clear /y
```

---

[:arrow_left: Regresar](https://github.com/m4lal0/cheatsheets)