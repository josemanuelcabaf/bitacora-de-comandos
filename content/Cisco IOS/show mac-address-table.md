---
Modo: Privilegiado
Acción: Mostrar tabla CAM
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#switch #show #switchL3 
### Sintaxis
```
R#show mac-address-table [opciones]
```
Para versiones más recientes del IOS:
```
R#show mac address-table [opciones]
```
Abreviatura: `sh mac add`

### Descripción de propósito/uso

Su objetivo principal es visualizar la **tabla de direcciones MAC** (también conocida como tabla CAM - Content Addressable Memory) que el switch ha construido dinámicamente. Este comando se utiliza para verificar qué direcciones MAC ha aprendido el switch, a través de qué puerto están conectadas y en qué VLAN residen.
### Parámetros
- `[opciones]`.- En este parámetro se puede poner
- **`address [dirección-mac]`**: Filtra la salida para mostrar información solo de una dirección MAC específica.
- **`interface [tipo/número]`**: Muestra solo las direcciones MAC aprendidas a través de una interfaz física o lógica específica.
- **`vlan [id-vlan]`**: Muestra únicamente las entradas asociadas a una VLAN en particular.
- **`dynamic`**: Filtra para mostrar solo las direcciones aprendidas automáticamente por el switch (no las configuradas estáticamente).
- **`static`**: Muestra las direcciones configuradas manualmente por el administrador.
### Ejemplo
```
R#show mac-address-table
```
## <span style="color:rgb(0, 112, 192)">Salida</span> 

![[Pasted image 20260615232635.png]]
- **Vlan**: Indica la red lógica (VLAN) a la que pertenece la dirección MAC.
- **Mac Address**: Es la dirección física de la tarjeta de red (NIC) del dispositivo conectado.
- **Type**:
    - **DYNAMIC**: El switch aprendió esta dirección observando el tráfico de origen que entra por sus puertos.
    - **STATIC**: Configurada manualmente por un administrador.
    - **CPU**: Indica que la dirección pertenece al propio switch o a un proceso interno.
- **Ports**: Indica el puerto físico (o lógico) donde el dispositivo está conectado.