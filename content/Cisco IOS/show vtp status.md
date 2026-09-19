---
Modo: Privilegiado
Acción: Mostrar información de protocolo
Propósito: Convergencia de VLANs
Tema: Muestra y Verificación
---
#switch  #switchL3  #VTP #show
### Sintaxis
```
R#show vtp status
```
### Descripción de propósito/uso

Este comando se utiliza para confirmar si el switch está operando correctamente dentro de un dominio VTP, identificar su modo de operación (Server, Client o Transparent) y verificar la versión del protocolo que está utilizando. Es vital para resolver problemas donde las VLANs no se propagan de un switch a otro.
### Ejemplo
```
Switch# show vtp status
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 
```
Switch# show vtp status
VTP Version                     : 2
Configuration Revision          : 5
Maximum VLANs supported locally : 1024
Number of existing VLANs        : 12
VTP Operating Mode              : Server
VTP Domain Name                 : Empresa_Red
VTP Pruning Mode                : Disabled
VTP V2 Mode                     : Disabled
```
### Explicación de los parámetros clave

- **VTP Version**: Indica la versión de VTP en uso (1, 2 o 3).
- **Configuration Revision**: **El parámetro más importante.** Es un número que aumenta cada vez que haces un cambio en las VLANs. Si conectas un switch nuevo, este debe tener un número de revisión menor o igual al del servidor, o podría sobrescribir la base de datos de VLANs de toda tu red.
- **VTP Operating Mode**:
    - **Server**: Puede crear, borrar y modificar VLANs; envía y sincroniza información.
    - **Client**: No puede modificar VLANs; solo recibe y sincroniza la base de datos del servidor.
    - **Transparent**: No participa en el VTP, pero reenvía los anuncios VTP a otros. Útil para mantener VLANs locales sin que se vean afectadas por cambios externos.
- **VTP Domain Name**: El nombre del dominio al que pertenece el switch. Todos los switches deben estar en el mismo dominio para sincronizarse.
- **VTP Pruning Mode**: Si está _Enabled_, el switch ahorra ancho de banda enviando tráfico de broadcast solo a los puertos que realmente tienen dispositivos en esa VLAN.
