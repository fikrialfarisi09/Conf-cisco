# VLAN configuration in routers and switches using Cisco Packet Tracer

ID VLAN = 100

IP      = 192.168.1.1/24

Router
  
  ↓
  
Switch
  
  ↓
  
  PC

# Router
configuration vlan in router

    Router>en
    Router#conf t
    Router(config)#int fa0/1.100
    Router(config-subif)# encapsulation dot1Q 100
    Router(config-subif)# ip address 192.168.1.1 255.255.255.0
    Router(config-subif)# Exit
    
# Switch
configuration vlan in switch

    switch>en
    switch# conf t
    switch(config)# int fa0/1
    switch(config-if)# switchport mode trunk
    switch(config-if)# exit
    switch(config)# int fa0/2
    switch(config-if)# switchport mode access
    switch(config-if)# switchport access vlan 100
    switch(config-if)# exit

# PC 
For PC, you just enter the IP address.

click pc -> click dekstop -> Ip configuration

IPV4 address    = 192.168.1.2
Subnet Mask     = 255.255.255.0
default gateway = 192.168.1.1
