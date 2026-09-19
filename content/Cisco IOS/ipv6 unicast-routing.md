---
Modo: Configuración global
Acción: Habilitar IPv6
Propósito: Enrutamiento IPV6
Tema: Enrutamiento
---
#router #switchL3  #IPv6 #estático #dinámico 
### Sintaxis
```
R(config)#ipv6 unicast-routing 
```
Abreviatura: `ipv6 uni`
### Descripción de propósito/uso

El comando **`ipv6 unicast-routing`** se ejecuta en el modo de configuración global de Cisco IOS y se utiliza para **habilitar el enrutamiento de paquetes IPv6** en el dispositivo. Por defecto, los routers Cisco vienen de fábrica preparados para enrutar tráfico IPv4, pero tienen las funciones de reenvío de tráfico IPv6 **desactivadas**. Si no configuras este comando, el equipo se comportará como un simple dispositivo final (host) IPv6: podrá tener IPs en sus puertos, pero **no pasará tráfico de una red a otra ni ejecutará protocolos de enrutamiento**
### Ejemplo
```
R(config)#ipv6 unicast-routing 
```

## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no ipv6 unicast-routing

### Sintaxis
```
R(config)#no ipv6 unicast-routing
```
Abreviatura: `no ipv6 uni`
### Descripción de propósito/uso
Desactiva por completo el enrutamiento IPv6, borrando la tabla de rutas IPv6 del sistema de inmediato.