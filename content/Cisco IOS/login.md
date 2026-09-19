---
Modo: Configuración específica
Acción: Autenticación
Propósito: Acceso
Tema: Conexión remota
---
#router #switch #switchL3  #telnet  
### Sintaxis
```
R(config-if)#login [local | authentication <nombre-de-lista>] 
```
Abreviatura: `no hay`
### Descripción de propósito/uso
Indica al dispositivo Cisco que, para permitir el acceso a través de esa línea (consola, SSH/Telnet vía VTY), debe autenticar al usuario, los parámetros "local" y "authentication" permiten hacerlo de dos maneras diferentes.
### Parámetros
- `[local]` .- Se coloca seguido del comando login, y con este en conjunto señala que la autenticación del usuario debe ser con la base de datos local configurada del equipo, solicitando usuario y contraseña.
- `[authentication]` .- Desacopla la línea de la autenticación local/simple y la asocia a un **perfil de autenticación AAA (Authentication, Authorization, Accounting)**. Permite usar servidores externos de directorio/control de accesos (**TACACS+** o **RADIUS**). Para esto, se necesita haber configurado AAA en el equipo. 
- `<nombre-lista>` .- Es la lista del grupo de servidores que se usará para el acceso (definir primero AAA)
- Solo `login`.- Utiliza la contraseña única configurada con `password <pass>` en esa misma línea (método antiguo/inseguro, sin usuario).
### Ejemplo

```
Router(config)# username admin secret cisco123
Router(config)# line vty 0 4
Router(config-line)# login local
```
## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no login

### Sintaxis
```
R(config-if)#no login
```
Abreviatura: `no hay`
### Descripción de propósito/uso
Permite el acceso directo a la línea **sin solicitar ninguna contraseña ni usuario** (equivalente a autenticación nula o abierta). **Limpia/Reemplaza** cualquier estado previo (`login`, `login local`, o `login authentication ...`).