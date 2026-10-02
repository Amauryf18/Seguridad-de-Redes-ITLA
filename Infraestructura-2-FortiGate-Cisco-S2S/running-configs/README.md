# Running-configs

R1-ISP:

version 15.2

hostname R1

no ip domain-lookup

interface GigabitEthernet0/0
 description ENLACE-HACIA-FIREWALL
 ip address 203.0.113.1 255.255.255.252
 no shutdown

interface GigabitEthernet0/1
 description ENLACE-HACIA-CISCO-VPN
 ip address 203.0.113.5 255.255.255.252
 no shutdown

ip route 203.0.113.0 255.255.255.252 203.0.113.5
ip route 10.3.3.0 255.255.255.0 203.0.113.5

end

R2-VPN:
hostname CISCO-VPN
no ip domain-lookup

interface GigabitEthernet0/0
 ip address 203.0.113.5 255.255.255.252
 no shutdown

interface GigabitEthernet0/1
 ip address 192.168.20.1 255.255.255.0
 no shutdown

ip dhcp excluded-address 192.168.20.1

ip dhcp pool SERVIDORES
 network 192.168.20.0 255.255.255.0
 default-router 192.168.20.1

ip route 10.3.3.0 255.255.255.0 203.0.113.6

access-list 110 permit ip 192.168.20.0 0.0.0.255 10.3.3.0 0.0.0.255

crypto isakmp policy 10
 encr des
 hash sha
 authentication pre-share
 group 2

crypto isakmp key VPN12345 address <IP-PUBLICA-OTRO-EXTREMO>

crypto ipsec transform-set VPN-SET esp-des esp-sha-hmac
 mode tunnel

crypto map VPN-MAP 10 ipsec-isakmp
 set peer <IP-PUBLICA-OTRO-EXTREMO>
 set transform-set VPN-SET
 match address 110

interface GigabitEthernet0/0
 crypto map VPN-MAP

end
