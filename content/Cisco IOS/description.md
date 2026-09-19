---
Modo: Configuración específica
Acción: Añadir descripción
Propósito: Administración
Tema: Configuración de interfaz
---
#router #switchL3  
### Sintaxis
```
R(config-if)#description [string] 
```
Abreviatura: `desc`
### Descripción de propósito/uso

Se utiliza dentro del modo de configuración de interfaz para **añadir un comentario de texto o etiqueta descriptiva** a un puerto. Es una práctica fundamental para que uno o cualquier otro administrador de red sepan exactamente a qué equipo, edificio o proveedor está conectado ese cable sin tener que rastrearlo físicamente.
### Parámetros
- `[string]` .- Poner una cadena de caracteres que representarán a la interfaz. Es decir, puedes poner cualquier texto identificativo. Se puede poner incluido espacios. Máximo 240 caracteres
### Ejemplo
```
R(config-if)#description ENLACE A Lan1 
```

## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no description

### Sintaxis
```
R(config-if)#no description
```
Abreviatura: `no desc`
### Descripción de propósito/uso
Quita cualquier texto asociado a la interfaz mediante el comando description.