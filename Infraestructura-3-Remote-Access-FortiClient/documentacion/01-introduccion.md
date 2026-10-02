# 01 - Introducción

## Propósito

Permitir que el usuario acceda al servidor web públicamente mediante HTTPS sin VPN, mientras que el acceso administrativo por SSH al servidor se permite únicamente cuando el usuario está conectado mediante SSL-VPN con FortiClient.

## Alcance

Esta infraestructura forma parte del laboratorio de Seguridad de Redes y se documenta de manera independiente, tal como exige la asignación.

## Objetivos específicos

1. Implementar la conectividad indicada por la infraestructura.
2. Configurar los elementos de seguridad requeridos.
3. Establecer el mecanismo VPN solicitado.
4. Comprobar la conectividad con pruebas reproducibles.
5. Evidenciar el comportamiento con la VPN activa e inactiva cuando corresponda.

## Tecnologías

- FortiGate
- GNS3
- Equipo de red indicado por la infraestructura
- Servidor Web
- VLAN 10
- DHCP
- NAT
- VPN/IPsec o SSL-VPN según la infraestructura
