_Data Center Leaf/Spine topology, VXLAN, MLAG, OSPF underlay_

**Configure Apline Hosts**

  ams-dc-host1
  
     docker exec -it clab-dc2-ams-dc-host1 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.210.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.210.0.1 dev eth1
     ping -i 30 10.210.0.102
     
  ams-dc-host2
  
     docker exec -it clab-dc2-ams-dc-host2 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.230.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.230.0.1 dev eth1
     ping -i 30 10.230.0.102

  ams-dc-host3
  
     docker exec -it clab-dc2-ams-dc-host3 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.210.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.210.0.1 dev eth1
     ping -i 30 10.210.0.102

  ams-dc-host4
  
     docker exec -it clab-dc2-ams-dc-host4 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.230.0.102 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.230.0.1 dev eth1
     ping -i 30 10.240.0.101

  ams-dc-host5
  
     docker exec -it clab-dc2-ams-dc-host5 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.220.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.220.0.1 dev eth1
     ping -i 30 10.220.0.102

  ams-dc-host6
  
     docker exec -it clab-dc2-ams-dc-host6 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.220.0.102 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.220.0.1 dev eth1
     ping -i 30 10.240.0.101

  ams-dc-host7
  
     docker exec -it clab-dc2-ams-dc-host7 sh
     apk update
     apk add net-tools iproute2 iputils-ping
     ifconfig eth1 10.240.0.101 netmask 255.255.255.0
     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.240.0.1 dev eth1
