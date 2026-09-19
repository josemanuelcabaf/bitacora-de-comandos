---
Modo: Variable
Acción: Configurar protocolo
Propósito: Convergencia
Tema: Conmutación
---
#switch #switchL3  #STP 
### Descripción de propósito/uso

Este protocolo modifica los parámetros relacionados al protocolo **STP y PVST** dentro de los switches. Los parámetros que puede tener son diversos y se configura principalmente en dos modos, el de configuración global y el de configuración de interfaz especifica.
```
R(config o config-if)#spanning-tree [argumento] 
```
Abreviatura: `span`
#### Argumentos de configuración global

Entre los argumentos se tiene:
1.  `vlan`.- Este parámetro decide qué switch es el "Root Bridge" (el centro jerárquico). Un valor más bajo es más preferido.
	 **Sintaxis**
```
R(config)#spanning-tree vlan [id] priority [value]
```
Donde `[id]` es el numero de la vlan y `[value]`  es el numero de prioridad de 2^0 a 2^16
2. `root`.- Definir prioridad para ser principal o de respaldo
	**Sintaxis**
```
R(config)#spanning-tree root [primary o secondary]
```
#### Argumentos de configuración especifica de interfaz

1. `portfast`.- hace que un puerto pase a estado de reenvío inmediatamente. Solo debe usarse en puertos donde hay dispositivos finales (PCs, impresoras, servidores)
	**Sintaxis**
	```
	R(config-if)#spanning-tree portfast
	```
2. `bpduguard`- Actúa como un guardaespaldas. Si alguien conecta otro switch a un puerto que tiene `portfast` activado, el switch recibirá una BDPU (mensaje de STP). Al tener `bpduguard` habilitado, el puerto se apagará automáticamente (err-disable) para proteger la red.
	**Sintaxis**
	```
	R(config-if)#spanning-tree bpduguard [enable o disable]
	```
3. `cost`.- Permite manipular artificialmente el costo del camino. Si tienes dos cables hacia el mismo lugar, pero se quiere que el tráfico prefiera uno sobre otro, se baja el costo en el puerto preferido.
	**Sintaxis**
	```
	R(config-if)#spanning-tree cost [value]
	```
	Donde `[value]` depende:
	- - **Método Short (16-bit):** Rango de **1 a 65,535** (predeterminado en estándares IEEE 802.1D antiguos).
	- **Método Long (32-bit):** Rango de **1 a 200,000,000** (predeterminado en redes modernas IEEE 802.1t para soportar puertos Gigabit y 10G)
4. `port-priority <valor>`.- Define qué puerto se prefiere si hay múltiples conexiones hacia el mismo switch vecino.
	**Sintaxis**
	```
	R(config-if)#spanning-tree port-priority [value]
	```
	Value depende de:
	- **Regla:** El valor más **bajo** es el más preferido.
    - **Rango:** 0 a 240 (siempre en incrementos de 16). El valor por defecto es **128**
### Ejemplo
```
Switch(config)# spanning-tree vlan 10 priority 4096
```

```
Switch(config)# interface GigabitEthernet 0/1 
Switch(config-if)# spanning-tree bpduguard enable
```