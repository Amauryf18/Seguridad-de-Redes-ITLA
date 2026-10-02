# 02 - Topología y direccionamiento

```mermaid
flowchart LR
    U[Usuarios<br/>VLAN 10<br/>10.3.3.0/24] --> FG1[FortiGate 1<br/>Cliente]
    FG1 --> ISP[ISP / Red pública]
    ISP --> FG2[FortiGate 2<br/>Servidor]
    FG2 --> W[Web Server<br/>192.168.10.0/24]
```

### Direccionamiento 

| Equipo | Dirección |
|---|---|
| FortiGate 1 WAN | `203.0.113.2/30` |
| Gateway ISP lado FG1 | `203.0.113.1/30` |
| FortiGate 2 WAN | `203.0.113.6/30` |
| Gateway ISP lado FG2 | `203.0.113.5/30` |
| Red de usuarios / lado cliente | `10.3.3.0/24` |
| Red del servidor / lado remoto | `192.168.10.0/24` |


## Diagrama final
<img width="726" height="542" alt="image" src="https://github.com/user-attachments/assets/3dffafb4-cf1f-43eb-9c65-ec93718bacf2" />


<img width="635" height="391" alt="image" src="https://github.com/user-attachments/assets/87d97f1d-fbac-4220-b836-fdef946f9e79" />

