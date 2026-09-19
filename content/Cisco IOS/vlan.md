---
Modo: Configuración global
Acción: Crear y modificar vlan
Propósito: Segmentación
Tema: VLANs
---
#switch #switchL3  
### Sintaxis
```
S(config)#vlan [id-vlan]
```
Abreviatura: `vl`
### Descripción de propósito/uso

Este comando permite crear y configurar Redes de Área Local Virtuales (VLANs) en switches Cisco. Cada VLAN tendrá su identificador numérico, por el cual se podrá identificar en otros switches cisco.
### Parámetros
- `[id-vlan]` .- Este argumento es el identificador numérico de la vlan a crear o configurar si ya estuviera creado. Este número puede ir desde 1 a 4049, donde el rango normal es de 1 a 1005 y el extendido es de 1006 a 4049. Las vlan 1 y 1002 a la 1005 son rangos reservados.
### Ejemplo
```
Switch(config)# vlan 20 
Switch(config-vlan)# name Marketing
```
### Comandos relacionados
Posterior a crear la vlan, se debería aplicar estos comandos: [[show vlan brief]], [[name]].
## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no vlan 

### Sintaxis
```
R(config)#no vlan [id-vlan]
```
Abreviatura: `no vl`
### Descripción de propósito/uso
Este comando sirve para eliminar la vlan con el identificador deseado. Si no se desasigna los puertos de la vlan antes de eliminar, estos quedarán inactivos o huérfanos, no podrán manejar el tráfico y no se verán en la tabla de vlan brief.
