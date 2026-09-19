---
Modo: Configuración específica
Acción: Asignar IP a interfaz
Propósito: Direccionamiento
Tema: Configuración de interfaz
---
#router #switchL3  #IPv4  
### Sintaxis
```
R(config-if)#ip address [opcional][ip address] [mask] 
```
Abreviatura: `ip ad`
### Descripción de propósito/uso
Se utiliza dentro del modo de configuración de interfaz para **asignar una dirección IPv4 estática y su respectiva máscara de subred** a un puerto físico o virtual.
### Parámetros
- `[ip address]` .- Dirección IPv4 en formato decimal
- `[mask]` .- Máscara de subred en formato decimal 
- `[opcional]`.- Este parámetro se pone en vez de los siguientes dos, normalmente es `dhcp`, para que la interfaz obtenga una dirección IPv4 de manera automática de un servidor DHCP.
### Ejemplo
```
R(config-if)# ip address 192.168.1.1 255.255.255.0
```
## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no ip address

### Sintaxis
```
R(config-if)#no ip address 
```
Abreviatura: `no ip ad`
No es necesario reescribir la ip ni la máscara
### Descripción de propósito/uso
Se utiliza dentro del modo de configuración de interfaz para eliminar la dirección IP que tiene asignado ese puerto.