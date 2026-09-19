---
Modo: Privilegiado
Acción: Mostrar info IPv4
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#router  #switchL3  #IPv4 
### Sintaxis
```
R#show ip interface 
```
Abreviatura: `sh ip int`
### Descripción de propósito/uso

Muestra la configuración técnica absoluta y detallada de **todas** las interfaces del equipo. Te mostrará por cada puerto: la IP, la máscara, si tiene listas de acceso (ACL) aplicadas, el estado del proxy ARP, temporizadores, configuraciones de seguridad y características de compresión.
### Ejemplo
```
R#show ip interface
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
```
GigabitEthernet0/1 is up, line protocol is up
  Internet address is 192.168.1.1/24
  Broadcast address is 255.255.255.255
  Address determined by setup command
  MTU is 1500 bytes
  Helper address is not set
  Directed broadcast forwarding is disabled
  Outgoing access list is not set
  Inbound  access list is ACL-SEGURIDAD
  Proxy ARP is enabled
  Local Proxy ARP is disabled
  Security level is default
  Split horizon is enabled
  ICMP redirects are always sent
  ICMP unreachables are always sent
  ICMP mask replies are never sent
  IP fast switching is enabled
  IP fast switching on the same interface is disabled
  IP Flow switching is disabled
  IP CEF switching is enabled
  IP CEF switching turbo vector
  IP Null turbo vector
  VPN Routing/Forwarding ratio is 0
  IP multicast fast switching is enabled
  IP multicast distributed fast switching is disabled
  IP route-cache flags are Fast, CEF
  Router Discovery is disabled
  IP output packet accounting is disabled
  IP access violation accounting is disabled
  TCP Header Compression is disabled
  RTP Header Compression is disabled
  Probe proxy name replies are disabled
  Policy routing is disabled
  Network address translation is disabled
  BGP Policy Mapping is disabled
  Input features: Access List
```

#### Relación con:
- [[Cisco IOS/show ip interface brief]]