---
Modo: Privilegiado
Acción: Mostrar tabla VLANs
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#switch #switchL3 #show
### Sintaxis
```
S#show vlan [specification] 
```
Abreviatura: `sh vl br`
### Descripción de propósito/uso

Su propósito principal es mostrar un **resumen rápido y ordenado** de todas las VLAN configuradas en el switch, indicando su número de identificación (ID), nombre, estado operativo y, lo más importante, **qué puertos de acceso físicos están asignados a cada VLAN**. A diferencia de ejecutar solo `show vlan` (que muestra parámetros avanzados, tipos de medios, MTU y campos largos difíciles de leer), el modificador `brief` recorta la salida
### Parámetros
- `[Specification]`.- Aquí se puede poner comandos para filtrar cierta parte de toda la información. (Pueden o no ponerse, no es obligatorio):
    - `brief` .- Resume o detalla más la información a mostrar de las VLANs. Muestra únicamente el ID, nombre, estado y los puertos de acceso asociados.
    - `id [id-vlan]` .- Se agrega después de `id` para que el sistema muestre solo la info de una vlan
    - `name [vlan-name]` .- Se agrega después de `name` para que el sistema muestre solo la info de la vlan que tenga ese nombre.
    - `summary`.- Muestra un recuento total de cuántas VLANs existen y qué tipos están activos en el dispositivo.
### Ejemplo
```
Switch# show vlan brief
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
```
VLAN Name                             Status    Ports
---- -------------------------------- --------- -------------------------------
1    default                          active    Gi0/1, Gi0/2, Gi0/3, Gi0/4
10   Ventas                           active    Gi0/5, Gi0/6
20   Marketing                        active    Gi0/7, Gi0/8
1002 default-vlan                     active    
1003 fddi-default                     active    
1004 token-ring-default               active    
1005 fddi-net-default                 active
```