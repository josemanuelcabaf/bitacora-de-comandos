---
Modo: Configuración global
Acción: Añadir ruta estática
Propósito: Enrutamiento IPv4
Tema: Enrutamiento
---
#router #switchL3  #IPv4 #estático
### Sintaxis
```
R(config)#ip route [red destino] [máscara destino] [interfaz out/ip next salto] [opc:Administrative distance]
```
Abreviatura: `ip ro` o `ip rou`
### Descripción de propósito/uso
Se utiliza en el modo de configuración global de Cisco IOS para **crear una ruta estática**. Esto le dice manualmente al router hacia qué dirección o interfaz debe enviar los paquetes de datos para llegar a una red remota específica.
### Parámetros
- `[red destino]` .- Se pone la red a la que se quiere llegar (no un host específico, sino la dirección de red)
- `[máscara destino]` .- Esto sirve para especificar la porción de red y host en la red de destino.
- `[interfaz out/ip next salto]` .- Se usa `interfaz de salida` cuando la topología entre routers es punto a punto. Se usa `ip del sig salto` cuando la topología es punto a miltipunto (debe descubrir por qué puerto mandar dada una ip destino del sgt. router)
- `[opc:Administrative distance]` .- Este campo es opcional, esto se utiliza principalmente para crear **rutas estáticas flotantes**, que sirven como respaldo si la ruta principal falla. Si no se pone, el sistema asume un 1. Este campo va de 0 a 255 (0 para las directamente conectadas).  A más bajo numero más confiable y viceversa.
### Ejemplo
```
RF(config)#ip route 200.87.100.96 255.255.255.240 Serial0/3/0
```
o con ip del siguiente salto y AD:
```
RF(config)#ip route 200.87.100.96 255.255.255.240 10.10.10.1 50
```
## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no ip route

### Sintaxis
```
R(config-if)#no ip route [red destino] [máscara destino] [interfaz out/ip next salto] [opc:Administrative distance]
```
Abreviatura: `no ip ro`
### Descripción de propósito/uso
Elimina una ruta estática específica. __OJO:__ Debes escribir exactamente la misma red, máscara, salto y en su caso AD que usaste al crearla para borrarla.