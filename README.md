# Duplex
 Duplex and Speed
 
 ![Duplex](Duplex.png)

### Switch 1
```
enable
configure terminal
hostname SW1
ip default-gateway 192.168.1.1
interface Vlan1
ip address 192.168.1.2 255.255.255.0
no shutdown
exit
interface FastEthernet0/ 1
duplex half
exit
interface FastEthernet0/ 2
duplex half
speed 10
```


### Switch 2
```
enable
configure terminal
hostname SW2
ip default-gateway 192.168.1.1
interface Vlan1
ip address 192.168.1.3 255.255.255.0
no shutdown
exit
interface FastEthernet0/ 1
speed 10
exit
interface FastEthernet0/ 2
speed auto
exit
interface FastEthernet0/ 2
duplex auto
exit
exit
```


### show interfaces SW1

```
int f0/1
Half-duplex, 100Mb/s
int f0/2
Half-duplex, 10Mb/s
int f0/3
 Full-duplex, 100Mb/s
 ```
 
 ### show interfaces SW2
 ```
 int f0/1
 Full-duplex, 10Mb/s
 int f0/2
 Full-duplex, 100Mb/s
 int f0/3
  Full-duplex, 100Mb/s
  ```











