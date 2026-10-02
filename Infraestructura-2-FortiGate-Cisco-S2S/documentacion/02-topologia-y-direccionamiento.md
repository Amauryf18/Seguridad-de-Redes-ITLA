# 02 - Topología y direccionamiento

```mermaid
flowchart LR
    U[Usuarios<br/>VLAN 10<br/>10.3.3.0/24] --> F[FortiGate]
    F --> I[Cisco / ISP<br/>203.0.113.5]
    I --> C[Equipo Cisco]
    C --> W[Web Server<br/>192.168.20.0/24]
```

### Direccionamiento de referencia utilizado en el laboratorio

# Direccionamiento IP – Topología 2

| Equipo / Red       | Dirección         |
| ------------------ | ----------------- |
| VLAN 10 – Usuarios | `10.3.3.0/24` |
| Gateway Usuarios   | `10.3.3.1`        |
| Red Servidores     | `192.168.20.0/24` |
| Gateway Servidores | `192.168.20.1` |
| Cisco VPN – WAN    | `203.0.113.5/30` |
| Peer Cisco VPN     | `203.0.113.6` |

> Verifica que estos valores coincidan exactamente con la topología final presentada en el video y con las capturas.


## Diagrama final
<img width="1024" height="641" alt="image" src="https://github.com/user-attachments/assets/cf829771-6c16-4dd1-a280-fd55996a4354" />

## Topologia
<img width="498" height="322" alt="image" src="https://github.com/user-attachments/assets/d6e4d53c-881f-462f-8a9d-b77f5863d738" />


