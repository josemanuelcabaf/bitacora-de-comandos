---
Modo: Privilegiado
Acción: Mostrar tabla enrutamiento
Propósito: Convergencia
Tema: Enrutamiento
---
#router #switchL3  #IPv4  #show
### Sintaxis
```
R#show ip route 
```
Abreviatura: `sh ip ro`
### Descripción de propósito/uso
Se ejecuta en el modo Privilegiado de Cisco IOS y se utiliza para **visualizar la tabla de enrutamiento IPv4 completa** del dispositivo (router o switchL3).
Esta tabla contiene todas las redes que el equipo conoce (ya sea de forma directa, estática o a través de protocolos dinámicos) y define exactamente por qué interfaz o hacia qué dirección IP se deben enviar los paquetes para llegar a su destino

### Ejemplo
```
R#sh ip route
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
```
Gateway of last resort is 10.0.0.2 to network 0.0.0.0

C    192.168.1.0/24 is directly connected, GigabitEthernet0/1
L    192.168.1.1/32 is directly connected, GigabitEthernet0/1
S    192.168.2.0/24 [1/0] via 10.0.0.2
O    172.16.0.0/16 [110/2] via 10.0.0.6, 00:15:23, GigabitEthernet0/2
S*   0.0.0.0/0 [1/0] via 10.0.0.2

```