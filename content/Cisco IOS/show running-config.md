---
Modo: Privilegiado
Acción: Mostrar archivo
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#router #switch #switchL3  #show
### Sintaxis
```
R#show running-config 
```
Abreviatura: `sh run`
### Descripción de propósito/uso
Este comando sirve para mostrar el archivo de configuración actual `running-config` guardado en la memoria RAM del router o switch. Esta configuración representa el estado operativo real y actual del equipo; cualquier cambio que realices se refleja aquí de forma inmediata. Al apagar o reiniciar el router, toda la información en el `running-config` se perderá a menos que la guardes.
### Ejemplo
```
R#show running-config
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
La salida es el archivo de configuración actual dividido por secciones.
## Variaciones

Para mostrar interfaces específicas (se aplican abreviaturas):
```
R#show running-config interface [tipo][numero]
```
Para filtrar información:
- Se utiliza la tubería`|`
```
R#show running-config | section [bloque o expresion regular] [especificación]
```
El router toma el texto que pongas al final en `[bloque o expresión regular]` y busca cualquier bloque de configuración cuyo encabezado (la primera línea) **coincida o contenga** ese texto y de ahí te mostrará todos los comando aplicados. Lo puedes especificar más con `[Especificación]`. Por ejemplo:
`sh run | s interface` (Te mostrará la configuración completa de la Interfaz 1, de la Interfaz 2, de la Interfaz 3, etc.)
`sh run | s interface g0/0` (Te mostrará únicamente el bloque de esa interfaz específica.)
