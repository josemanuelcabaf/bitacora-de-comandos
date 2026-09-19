---
Modo: Configuración específica
Acción: Asignar IP a interfaz
Propósito: Direccionamiento
Tema: Configuración de interfaz
---
#router #switchL3 #IPv6  #estático 
### Sintaxis
```
R(config-if)#ipv6 address [prefijo]/[longitud de prefijo] [opc: "link-local", "eui-64"]
```
Abreviatura: `ipv6 ad`
La / es parte de la estructura del comando
### Descripción de propósito/uso
El comando **`ipv6 address`** se ejecuta dentro del modo de configuración de interfaz para **asignar una dirección IPv6 (ya sea #GUA o de #LLA) a un puerto** del dispositivo. A diferencia de IPv4, una misma interfaz Cisco puede tener **múltiples direcciones IPv6 válidas configuradas al mismo tiempo** sin que una borre a la otra
### Parámetros
- `[prefijo]` .- Se pone la dirección IP que se desea asignar a esta interfaz
- `[longitud del prefijo]` .- Se indica con esto la cantidad de bits que pertenecen a la parte de prefijo (o de red en IPv4)
- `[link local]` (opcional).- Se usa para asignar una #LLA, que sirven para la comunicación dentro de la misma red local. Si no se pone, se asigna como global unicast.
- `[eui-64]` (opcional).- Se usa para indicar al router que use el prefijo de /64 y que lo demás lo forme con su MAC a través del proceso EUI-64.
	- `[autoconfig]` (opcional).- Configura la interfaz para que obtenga su dirección de manera automática a través de los mensajes de un router vecino (SLAAC).
### Ejemplo
```
Router(config-if)#ipv6 address 2001:db8:acad:1::1/64
```

```
Router(config-if)#ipv6 address fe80::1/64 link-local
```

## <span style="color:rgb(192, 0, 0)">Opuesto</span>: comando

### Sintaxis
```
R(config-if)#no ipv6 address [IP/Prefijo]
```
Abreviatura: `no ipv6 add`
### Descripción de propósito/uso
Elimina esa dirección específica de la interfaz. Si tienes varias IPs en el puerto, debes especificar cuál deseas borrar para no afectar a las demás