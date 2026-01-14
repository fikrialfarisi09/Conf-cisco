# How create dhcp in router using cisco packet tracer

Ipv4 Address = 192.168.1.1/24

Router

  ↓
  
Switch

  ↓

PC , PC

# Router 
Configuration router

    router> en
    router# conf t
    router(config)# int fa0/0
    router(config-if)# ip add 192.168.1.1 255.255.255.0
    router(configif)# exit
    router(config)#ip dhcp pool name
    router(dhcp-config)# network 192.168.1.0 255.255.255.0
    router(dhcp-config)# default-router 192.168.1.1
    router(dhcp-config)# exit 

# PC

    
