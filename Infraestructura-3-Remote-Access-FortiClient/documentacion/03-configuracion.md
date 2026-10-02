# 03 - Configuración

## 1. Red
Documentar por GUI:
- WAN del FortiGate.
- LAN.
- Ruta por defecto.
- NAT.
- Red del servidor.

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

## 6. Pruebas
### Sin VPN
- HTTPS al servidor: debe funcionar.
- SSH al servidor: debe estar bloqueado/no permitido desde Internet.

### Con VPN
- FortiClient conectado.
- Cliente recibe una IP del pool VPN.
- SSH hacia `10.3.3.2` funciona.
- Traceroute puede utilizarse como evidencia de conectividad.

## 7. Evidencia
Capturar:
- FortiClient conectado.
- IP asignada por VPN.
- Política VPN→SSH.
- Sesión SSH.
- HTTPS público.
- Prueba de SSH antes de conectar VPN.


## Capturas recomendadas

Guarda las capturas en `imagenes/` con nombres descriptivos, por ejemplo:

- `01-interfaces.png`
- `02-rutas.png`
- `03-nat.png`
- `04-vpn-phase1.png`
- `05-vpn-phase2.png`
- `06-firewall-policy.png`
- `07-dhcp.png`

Usa las capturas reales de tu laboratorio. No reemplaces evidencia real por imágenes genéricas.
