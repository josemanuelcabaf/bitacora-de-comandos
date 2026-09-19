---
Modo: Configuración específica
Acción: Prender interfaz
Propósito: Levantar conexión
Tema: Configuración de interfaz
---
#router #switchL3 #IPv4 #IPv6 
### Sintaxis
```
R(config-if)#no shutdown 
```
Abreviatura: `no shut` o `no sh`
### Descripción de propósito/uso
Activa la interfaz. Por defecto, las interfaces en los routers y switches capa 3 Cisco vienen administrativamente apagadas por motivos de seguridad. Este comando cambia el estado administrativo a activo o up.
### Ejemplo
```
R(config-if)#no shutdown 
```

## <span style="color:rgb(192, 0, 0)">Opuesto</span>: shutdown

### Sintaxis
```
R(config-if)#shutdown
```
Abreviatura: `shut` o `sh`
### Descripción de propósito/uso
Este comando se utiliza para apagar administrativamente la interfaz en la que se está configurando. Cambia su estado a down.