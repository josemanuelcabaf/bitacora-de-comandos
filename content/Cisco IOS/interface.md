---
Modo: Configuración global
Acción: Escalar modo
Propósito: Navegación
Tema: Configuración de interfaz
---
#router #switch #IPv4 #IPv6  
### Sintaxis
```
R(config)#interface [tipo] [número] 
```
Abreviatura: `int` o `i`
puede no haber espacio entre tipo y numero
### Descripción de propósito/uso
Este comando se utiliza para ingresar al modo de configuración de interfaz. Desde este modo, puedes modificar el estado físico y lógico de un puerto específico, como asignarle una dirección IP, encenderlo o cambiar su velocidad.
### Parámetros
- `[tipo]` .- Nombre de la interfaz y abreviatura, por ejemplo:

| Nombre de la interfaz                   | Abreviatura comun |
| --------------------------------------- | ----------------- |
| `Ethernet` (10 Mbps)                    | `e`               |
| `FastEthernet` (100 Mbps)               | `f` o `fa`        |
| ``GigabitEthernet`` (1 Gbps)            | `g` o `gi`        |
| ``TenGigabitEthernet``(10 Gbps)         | `te`              |
| ``Loopback`` (Interfaz virtual)         | `lo`              |
| ``Vlan`` (Interfaz de Switch Virtual)   | `vl`              |
| `Serial` (Conexiones WAN antiguas)      | `s` o `se`        |
| `Port-Channel` (Agregación de enlaces)` | `po`              |
- `[numero]` .- Aquí se pone el numero que identifica a la interfaz, por ejemplo `0/0` o `0/1/0` etc.
### Ejemplo
```
R(config)#interface FastEthernet0/2
R(config-if)#
```
O en su caso con abreviaturas
```
R(config)#interface fa0/2
```
