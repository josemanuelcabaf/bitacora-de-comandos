---
Modo: Privilegiado
Acción: Mostrar información física
Propósito: Administración
Tema: Muestra y Verificación
---
#router #switch #switchL3  #show
### Sintaxis
```
R#show controller [tipo-de-interfaz] [num-de-interfaz] [modificador]
```
Abreviatura: `Si la hay`
### Descripción de propósito/uso
Este comando muestra información de diagnóstico a nivel de hardware y de la capa física de las interfaces de red en dispositivos como routers y switches. Sirve principalmente para solucionar problemas profundos de conexión y hardware. La información que muestre sobre cada interfaz será específica del tipo de interfaz.
### Parámetros
- `[modificador]` .- Puede ser usado pra mostrar información especifica de la salida del comando:
	- `summary`.- Ofrece una vista resumida del estado de todos los controladores de hardware en lugar de páginas completas de códigos y registros.
	- `stats`.- Muestra contadores detallados de errores físicos, tramas descartadas a nivel de chip o problemas acumulados de transmisión.
	- `brief`.- Reduce el nivel de detalle técnico para mostrar únicamente los datos operativos básicos del hardware de la interfaz.
- `[tipo-de-interfaz]` .- Se puede especificar el tipo de interfaz de la cual se quiere obtener información de capa física
- `[num-de-interfaz]` .- Es el numero de interfaz especifico del cual se quiere información
### Ejemplo
```
show controllers serial 0/0/0
```

