ssh R1_main@172.20.20.20

/interface vlan
add interface=ether2 name=vlan10 vlan-id=10
add interface=ether2 name=vlan20 vlan-id=20
/interface wireless security-profiles
set [ find default=yes ] supplicant-identity=MikroTik
/ip pool
add name=pool10 ranges=192.168.100.2-192.168.100.254
add name=pool20 ranges=192.168.120.2-192.168.120.254
/ip dhcp-server
add address-pool=pool10 disabled=no interface=vlan10 name=server1
add address-pool=pool20 disabled=no interface=vlan20 name=server2
/ip address
add address=172.31.255.30/30 interface=ether1 network=172.31.255.28
add address=192.168.100.1/24 interface=vlan10 network=192.168.100.0
add address=192.168.120.1/24 interface=vlan20 network=192.168.120.0
/ip dhcp-client
add disabled=no interface=ether1
/ip dhcp-server network
add address=192.168.100.0/24 gateway=192.168.100.1
add address=192.168.120.0/24 gateway=192.168.120.1
/system identity
set name=RO1


ssh SW_1@172.20.20.21

/interface bridge
add name=bridge10
add name=bridge20
/interface vlan
add interface=ether2 name=vlan10 vlan-id=10
add interface=ether2 name=vlan20 vlan-id=20
add interface=ether3 name=vlan110 vlan-id=10
add interface=ether4 name=vlan220 vlan-id=20
/interface wireless security-profiles
set [ find default=yes ] supplicant-identity=MikroTik
/interface bridge port
add bridge=bridge10 interface=vlan10
add bridge=bridge20 interface=vlan20
add bridge=bridge10 interface=vlan110
add bridge=bridge20 interface=vlan220
/ip address
add address=172.31.255.30/30 interface=ether1 network=172.31.255.28
/ip dhcp-client
add disabled=no interface=ether1
add disabled=no interface=bridge10
add disabled=no interface=bridge20
/system identity
set name=SWO01.L3.01



ssh SW_2@172.20.20.22


/interface bridge
add name=bridge10
/interface vlan
add interface=ether2 name=vlan10 vlan-id=10
/interface wireless security-profiles
set [ find default=yes ] supplicant-identity=MikroTik
/interface bridge port
add bridge=bridge10 interface=vlan10
add bridge=bridge10 interface=ether3
/ip address
add address=172.31.255.30/30 interface=ether1 network=172.31.255.28
/ip dhcp-client
add disabled=no interface=ether2
add disabled=no interface=bridge10
/system identity
set name=SWO02.L3.01


ssh SW_3@172.20.20.23


/interface bridge
add name=bridge20
/interface vlan
add interface=ether2 name=vlan20 vlan-id=20
/interface wireless security-profiles
set [ find default=yes ] supplicant-identity=MikroTik
/interface bridge port
add bridge=bridge20 interface=vlan20
add bridge=bridge20 interface=ether3
/ip address
add address=172.31.255.30/30 interface=ether1 network=172.31.255.28
/ip dhcp-client
add disabled=no interface=ether1
add disabled=no interface=bridge20
/system identity
set name=SWO02.L3.02



