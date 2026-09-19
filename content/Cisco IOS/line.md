---
Modo: Configuración global
Acción: Configurar línea
Propósito: Administración
Tema: Conexión remota
---
#router #telnet #switch #switchL3   
### Sintaxis
```
R(config)#line [tipo-de-puerto] [primer-puerto] [último-puerto]
```
Abreviatura: `li`
### Descripción de propósito/uso

Su propósito principal es **configurar las líneas de comunicación o puertos de acceso al sistema operativo del dispositivo**, como la consola o los puertos de acceso remoto vty.
### Parámetros
- `[tipo-de-puerto]` .- Es el tipo de puerto que entrarás a modificar dentro del sistema operativo: `con` (puerto de consola - usualmente seguido de un `0`), `aux` (puerto auxiliar - usaba para módems de dial-up - usualmente seguido de un cero), `vty` (Terminal virtual - los puertos pueden ir de 0 a 15)
- `[primer-puerto]` .- El número de la línea inicial que deseas configurar (por ejemplo, `0`).
- `[último-puerto]` .- (Opcional) Permite configurar un rango de líneas de manera simultánea. Muy común en las líneas `vty` (por ejemplo, `line vty 0 4` para configurar las primeras 5 sesiones remotas simultáneas).
### Ejemplo
```
Switch(config)# line vty 0 4 
Switch(config-line)#
```

