---
Modo: Configuración global
Acción: Crear usuario y contraseña
Propósito: Acceso
Tema: Conexión remota
---
#Router #switch #switchL3 #Telnet #IPv4 #IPv6 
### Sintaxis
```
R(config)#username [nombre] privilege [number] (pass/secret) [tipo de cifrado] [contraseña] 
```
Abreviatura: `user o usern`
### Descripción de propósito/uso
Se utiliza en la gestión de usuarios locales en un dispositivo de red como routers o switches. . Se utiliza principalmente para crear, modificar o eliminar cuentas de usuario locales en el router, las cuales son necesarias para la autenticación en procesos como el acceso por consola, Telnet, SSH, o para la autorización en diferentes niveles de privilegios.
### Parámetros
- `[nombre]` .- Aquí se introduce el nombre de usuario con el que se iniciará sesión por telnet, ssh u otro (es sensible a mayusculas y minusculas)
- `[number]` .- se introduce un número de 0 a 15, el cual indica el privilegio del usuario (qué comandos iniciales podrá utilizar). Predefinidos están el 0 (muy básico, solo conexión y monitoreo), el 1 (modo por defecto al iniciar sesión o user), y el 15 (Maximo privilegio - todos los comandos). Los niveles personalizables son del 2 al 14
- `(pass/secret)` .- Se escribe o **password** o **secret**, lo cual sirve para introducir una contraseña con el cual se iniciará sesión luego de haber introducido el nombre de usuario (la contraseña es especifica de cada usuario). Password no encripta, secret sí
- `[tipo de cifrado]` .- Es como se encriptará la contraseña introducida. Para secret hay: MD5 (tipo 5), SHA-256 (tipo 8) y Scrypt (tipo 9). Para Password hay: Texto plano (tipo 0) y cifrado débil (tipo 7). En el comando se pone el numero, si no se pone se asume con secret el mejor y password el 0
- `[contraseña]` .- Se introduce una cadena de caracteres que servirá como la contraseña del usuario creado 
### Ejemplo
```
Router(config)# username administrador privilege 15 secret SuperClaveSegura123!
```
## <span style="color:rgb(192, 0, 0)">Opuesto</span>: no username

### Sintaxis
```
R(config-if)#no username [nombre de usuario existente]
```
### Descripción de propósito/uso
Para eliminar un usuario creado previamente de la base de datos local del router, se utiliza la forma negada del comando anteponiendo **`no`** Si lo haces si el no, el usuario simplemente se modificará (sobrescribirá)