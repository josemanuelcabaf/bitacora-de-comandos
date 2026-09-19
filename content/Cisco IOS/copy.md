---
Modo: Privilegiado
Acción: Guardar
Propósito: Memoria
Tema: Comandos básicos
---
#router  #switch 
### Sintaxis
```
R#copy [archivo origen a copiar] [archivo destino de copiado] 
```
Abreviatura: `cop`
### Descripción de propósito/uso
El comando **`copy`** en Cisco IOS es una herramienta fundamental que se utiliza para copiar, respaldar o restaurar archivos entre diferentes ubicaciones del dispositivo o hacia servidores externos. Este comando normalmente se utiliza para guardar la configuración actual en la configuración de inicio para que el router o switch la utilice en el próximo encendido
### Parámetros
- `[archivo origen a copiar]` .- Es el archivo que se copiará, lo que se escribirá. Normalmente es el archivo `running-config` o abreviado `run`
- `[archivo destino de copiado]` .- Es el donde se escribirá, cual es el archivo donde se copiará el origen. Normalmente es el archivo `startup-config` o abreviado `start`                                                                                                      
### Ejemplo
```
R#copy running-config startup-config
```

