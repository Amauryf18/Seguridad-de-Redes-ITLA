# 04 - Pruebas y evidencias

## Objetivo de las pruebas

Demostrar con evidencia que la infraestructura cumple el objetivo de seguridad indicado.

## Evidencias

## 1. FortiGate
Documentar por GUI:
- Interfaces.
- VLAN 10.
- DHCP.
- Ruta por defecto.
- NAT.
- Políticas de firewall.
- VPN/IPsec.

## 2. Equipo Cisco
Documentar:
- Interfaces.
- Direccionamiento.
- Rutas.
- NAT, si fue utilizado.
- Configuración IPsec.
- ACL/crypto ACL utilizada para identificar el tráfico protegido.

## 3. VPN Site-to-Site
El tráfico protegido debe corresponder a:
- Local: `10.10.10.0/25`
- Remota: `10.10.20.0/28`

## 4. Pruebas
- `ping` del usuario al servidor.
- `tracert`/`traceroute`.
- Acceso HTTPS.
- Estado del túnel.
- Desactivar la VPN y repetir la prueba.
- Evidenciar la diferencia.

## 5. Seguridad
Explicar cómo el túnel protege la comunicación entre redes y cómo las políticas/rutas evitan que la prueba dependa de una conexión directa no protegida.

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
