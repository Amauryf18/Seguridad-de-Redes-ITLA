# 02 - Topología y direccionamiento

```mermaid
flowchart LR
    U[Usuarios<br/>VLAN 10<br/>10.3.3.0/24] --> FG1[FortiGate 1<br/>Cliente]
    FG1 --> ISP[ISP / Red pública]
    ISP --> FG2[FortiGate 2<br/>Servidor]
    FG2 --> W[Web Server<br/>192.168.10.0/24]
```

### Direccionamiento registrado durante el laboratorio

| Equipo | Dirección |
|---|---|
| FortiGate 1 WAN | `203.0.113.2/30` |
| Gateway ISP lado FG1 | `203.0.113.1/30` |
| FortiGate 2 WAN | `203.0.113.6/30` |
| Gateway ISP lado FG2 | `203.0.113.5/30` |
| Red de usuarios / lado cliente | `10.3.3.0/24` |
| Red del servidor / lado remoto | `192.168.10.0/24` |

> **Importante:** la consigna académica solicita usuarios `/25`, VLAN 10 y servidor `/28`. Antes de entregar, sustituye en esta tabla cualquier direccionamiento de laboratorio que haya sido posteriormente cambiado por el direccionamiento final basado en tu matrícula.


## Diagrama final

Guarda en `diagramas/` una imagen exportada del diagrama final de GNS3.

Ejemplo de nombre:

`topologia-final.png`
