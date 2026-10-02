# Running-configs

# 03 - Configuración

## 1. Configuración de red
Sw1:!
hostname SW-TOPOLOGIA1
!
no ip domain-lookup
!
vlan 10
 name USUARIOS
!
interface GigabitEthernet0/0
 description TRUNK-HACIA-FIREWALL-1
 switchport mode trunk
 switchport trunk allowed vlan 10
 no shutdown
!
interface GigabitEthernet0/1
 description CONEXION-USUARIO
 switchport mode access
 switchport access vlan 10
 spanning-tree portfast
 no shutdown
!
end

R1-ISP:
hostname R-TOPOLOGIA1
!
no ip domain-lookup
!
!
interface GigabitEthernet0/0
 description ENLACE-WAN-HACIA-FIREWALL-1
 ip address 203.0.113.1 255.255.255.252
 no shutdown
!
!
interface GigabitEthernet0/1
 description ENLACE-WAN-HACIA-FIREWALL-2
 ip address 203.0.113.5 255.255.255.252
 no shutdown
!
!
