# 04 - Pruebas y evidencias

## Objetivo de las pruebas

Demostrar con evidencia que la infraestructura cumple el objetivo de seguridad indicado.

## Evidencias

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


## Registro de pruebas

| # | Prueba | Resultado | Evidencia |
|---|---|---|---|
| 1 | Estado de interfaces | PENDIENTE DE EVIDENCIA | `evidencias/` |
| 2 | Conectividad IP | PENDIENTE DE EVIDENCIA | `evidencias/` |
| 3 | Estado VPN | PENDIENTE DE EVIDENCIA | `evidencias/` |
| 4 | HTTPS | PENDIENTE DE EVIDENCIA | `evidencias/` |
| 5 | Traceroute | PENDIENTE DE EVIDENCIA | `evidencias/` |
| 6 | Prueba con VPN inactiva | PENDIENTE DE EVIDENCIA | `evidencias/` |

> Cambia cada resultado a APROBADO/NO APROBADO únicamente después de realizar la prueba real.
