# 03 - Configuración

## 1. Configuración de red
Documentar con capturas:
- Interfaces WAN y LAN.
- Direccionamiento IP.
- Rutas necesarias.
- VLAN 10 y gateway.
- DHCP para usuarios.

## 2. NAT
Documentar:
- NAT de salida a Internet.
- Excepción/no NAT para el tráfico protegido por la VPN, cuando corresponda.

## 3. VPN Site-to-Site
Documentar:
- Phase 1.
- Phase 2.
- Redes locales y remotas.
- Autenticación y parámetros criptográficos.
- Estado del túnel.

## 4. Políticas de firewall
Documentar las políticas que permiten el tráfico entre las redes protegidas.

## 5. Pruebas
- Ping con VPN activa.
- Traceroute con VPN activa.
- Acceso HTTPS al servidor.
- Desactivar el túnel.
- Repetir las pruebas.
- Evidenciar que la comunicación deja de funcionar o deja de utilizar el túnel.

## 6. Seguridad
Explicar que el objetivo no es simplemente establecer conectividad, sino demostrar que el acceso entre las redes depende del túnel protegido.

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
