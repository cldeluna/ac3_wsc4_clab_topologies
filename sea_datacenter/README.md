_Data Center Leaf/Spine VXLAN topology with BGP underlay_

**Configure Apline Hosts**

  Connect to host
  
     docker exec -it clab-dc1-sea-dc-XXXX sh
     
  Update and configure host IP address

     apk update

     apk add net-tools iproute2 iputils-ping

     ifconfig eth1 10.XXX.0.XX netmask 255.255.255.0

     route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.XXX.0.1 dev eth1

     ping -i 30 XXX.XXX.XXX.XXX
