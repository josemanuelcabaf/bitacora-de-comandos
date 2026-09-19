---
Modo: Privilegiado
Acción: Mostrar info IPv4
Propósito: Información de confg.
Tema: Muestra y Verificación
---
#router #switchL3  #show #IPv4 
### Sintaxis
```
R#show ip interface brief 
```
Abreviatura: `sh ip int br`
### Descripción de propósito/uso
### Parámetros
- `Parametro 1` .- Descripción de uso
- `Parametro 2` .- Descripción de uso
- `Parametro 3` .- Descripción de uso
- `Parametro 4` .- Descripción de uso
### Ejemplo
```
Poner ejemplo
```
## <span style="color:rgb(0, 112, 192)">Salida</span>

| Interface          | IP-address  | Ok? | Method | Status              | Protocol |
| ------------------ | ----------- | --- | ------ | ------------------- | -------- |
| GigabitEthernet0/0 | 191.168.1.1 | YES | Manual | Administratively up | up       |
- **Interface:** Nombre del puerto.
- **IP-Address:** La dirección asignada (o `unassigned` si no tiene).
- **Method:** Cómo obtuvo la IP (`manual` si la escribiste tú, o `DHCP`, o `unset` si no ha sido puesta).
- **Status:** Estado físico de la capa 1. Si dice `administratively down`, significa que le falta el comando `no shut`. Si dice `up`, el cable está conectado eléctricamente.
- **Protocol:** Estado lógico de la capa 2. Es `down` o `up`. Debe estar en `up` para que pasen los datos.