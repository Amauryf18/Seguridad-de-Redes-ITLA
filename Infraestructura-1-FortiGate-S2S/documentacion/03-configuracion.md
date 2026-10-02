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
end

## 2. NAT
Documentar:
<img width="1361" height="69" alt="image" src="https://github.com/user-attachments/assets/3ea30cf0-1c9c-413e-9e1e-f287c375f8df" />


## 3. VPN Site-to-Site
<img width="1349" height="93" alt="image" src="https://github.com/user-attachments/assets/cd16b600-ad9b-40be-840b-200bd6d5c5cf" />

## 4. Políticas de firewall
<img width="1330" height="395" alt="image" src="https://github.com/user-attachments/assets/51a0b3b1-78c9-464f-bfe7-f4287e1f1d33" />


## 5. Pruebas
<img width="1227" height="831" alt="image" src="https://github.com/user-attachments/assets/7b0ba890-7e3a-4c8a-995d-765a4a3a08f0" />

