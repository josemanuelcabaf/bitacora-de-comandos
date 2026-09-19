---
Modo: Configuración específica
Acción: Añadir nombre
Propósito: Personalización
Tema: VLANs
---
#switchL3 #switch
### Sintaxis
```
S(config-vlan)#name [nombre-vlan]
```
Abreviatura: `na`
### Descripción de propósito/uso

Su propósito principal es **asignar una etiqueta de texto descriptiva a una VLAN específica** (por ejemplo, "Ventas", "Gerencia", "IoT" o "Invitados"). Por defecto, si creas una VLAN (como la VLAN 20) sin usar este comando, Cisco le asignará un nombre genérico automático (usualmente `VLAN0020`).
### Parámetros
- `[nombre-vlan]` .- Se pone aquí la cadena de caracteres que identificará a la vlan creada. Longitud máxima de 32 caracteres. Se recomienda usar guiones o guiones bajos en vez de espacios en blanco para evitar la no compatibilidad en otros sistemas.
### Ejemplo
```
Switch(config)# vlan 20 
Switch(config-vlan)# name Marketing
```

## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no name

### Sintaxis
```
S(config-vlan)#no name [nombre-vlan]
```
Abreviatura: no na`
### Descripción de propósito/uso
Cuando ejecutas `no name` dentro de la configuración de una VLAN, esta pierde la etiqueta que tenía (por ejemplo, "Ventas") y el switch automáticamente vuelve a nombrarla con su formato genérico por defecto, el cual sigue la estructura `VLANxxxx`