---
Modo: Configuración global
Acción: Configurar protocolo
Propósito: Convergencia
Tema: Conmutación
---
#switch #switchL3  #STP 
### Sintaxis
```
R(config)#spanning-tree mode [protocolo-a-usar] 
```
Abreviatura: `span mode`
### Descripción de propósito/uso

Este comando configura el switch para operar bajo el protocolo **Rapid Per-VLAN Spanning Tree (RPVST+)** de propiedad de cisco, donde cada VLAN tendrá su propia instancia independiente de RSTP. A diferencia del STP estándar que puede tardar hasta 50 segundos en recuperarse de un cambio en la topología, RPVST+ utiliza mecanismos de "propuesta y acuerdo" que permiten que los puertos pasen a estado de reenvío casi instantáneamente.
### Parámetros
- `protocolo-a-usar` .- Hay varios
  -  **`pvst`**: Protocolo Per-VLAN Spanning Tree original (estándar antiguo).
  - **`rapid-pvst`**: Protocolo Rapid Per-VLAN Spanning Tree (recomendado para la mayoría de las redes modernas).
  - **`mst`**: Multiple Spanning Tree (para entornos con cientos de VLANs, optimiza el uso de CPU).
### Ejemplo
```
Switch> enable 
Switch# configure terminal 
Switch(config)# spanning-tree mode rapid-pvst 
Switch(config)# end 
Switch# show spanning-tree summary
```

Relacionado está el comando   para que un puerto no participe en la negociación STP, por ejemplo de un dispositivo terminal