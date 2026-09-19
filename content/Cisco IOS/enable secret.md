---
Modo: Configuración global
Acción: Crear contraseña
Propósito: Acceso
Tema: Conexión remota
---
#router #switch #switchL3  #telnet 
### Sintaxis
```
Router(config)# enable secret [level <nivel>] [tipo_cifrado] [contraseña]
```
Abreviatura: `en s o ena se`
### Descripción de propósito/uso
### Parámetros
- `[contraseña]` .- Se introduce una cadena de caracteres que se solicitará cuando un usuario quiera acceder desde el modo de usuario al modo privilegiado, es decir escalar privilegios.
- `[level <nivel>]`.- Es opcional, pero especifica el nivel (0 a 15) al que se quiere poner contraseña
- `[tipo_cifrado]`.- Esto se ve ya en el comando [[username]]
### Ejemplo
```
Router(config)# enable secret SuperAdminClave2026!
```

