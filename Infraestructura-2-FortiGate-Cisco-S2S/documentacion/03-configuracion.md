# 03 - Configuración

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
