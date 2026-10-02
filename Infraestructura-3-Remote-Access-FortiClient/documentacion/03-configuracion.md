# 03 - Configuración

## 1. Red
Documentar por GUI:
FGT:
<img width="616" height="240" alt="image" src="https://github.com/user-attachments/assets/ac2aa151-9f0c-453b-b256-d663c2a01a0e" />
Interfaces:
<img width="680" height="175" alt="image" src="https://github.com/user-attachments/assets/eb64130d-fec8-47d7-89ea-366c4e69ccf0" />

## 2. Publicación HTTPS
Explicar el flujo:
`148.255.246.228:443 → Huawei → 10.0.0.212:443 → VIP → 10.3.3.2:443`

El objetivo es demostrar que HTTPS funciona sin VPN.

## 3. SSL-VPN Remote Access
Documentar:
- SSL-VPN habilitado.
- Interfaz WAN.
- Puerto `10443`.
- Pool `10.250.250.0/24`.
- Usuario/grupo.
- Portal.
- DNS.
- Certificado.

## 4. Política VPN → servidor
Política:
- Entrada: `ssl.root`
- Salida: `LAN`
- Usuario/grupo: grupo autorizado para VPN.
- Destino: `IP-SERVER` (`10.3.3.2/32`)
- Servicio: `SSH`
- Acción: `ACCEPT`
- NAT: desactivado.

## 5. Seguridad
No crear una política WAN → servidor que permita SSH directamente.
La intención es:
- HTTPS: público.
- SSH: únicamente mediante VPN.

### Con VPN
- FortiClient conectado.
- Cliente recibe una IP del pool VPN.
- SSH hacia `10.3.3.2` funciona.
- Traceroute puede utilizarse como evidencia de conectividad.


0
