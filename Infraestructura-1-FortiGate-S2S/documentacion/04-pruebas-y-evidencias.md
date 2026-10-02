# 04 - Pruebas y evidencias

## Objetivo de las pruebas

Demostrar con evidencia que la infraestructura cumple el objetivo de seguridad indicado.

## Evidencias

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
