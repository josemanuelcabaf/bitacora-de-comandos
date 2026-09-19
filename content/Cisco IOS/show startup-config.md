---
Modo: Privilegiado
Acción: Mostrar archivo
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#router #switch #switchL3 #show
### Sintaxis
```
R#show startup-config
```
Abreviatura: `sh sta` o `sh start`
### Descripción de propósito/uso
El comando **`show startup-config`** se ejecuta en el modo Privilegiado de Cisco IOS y se utiliza para **visualizar la configuración de respaldo almacenada en la memoria NVRAM** (Non-Volatile Random Access Memory), o en la memoría flash en el caso de los switches.
### Ejemplo
```
R#sh startup-config
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
Es el archivo de configuración actual por secciones.
## Variaciones
Igual que en [[Cisco IOS/show running-config]]