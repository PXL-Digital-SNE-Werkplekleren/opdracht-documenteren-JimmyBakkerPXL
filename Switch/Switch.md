# Switch Configuratie

<details class="details-section">
	<summary class="section-summary">Switch Configuratie</summary>

```
Current configuration : 1804 bytes
!
version 15.0
no service timestamps log datetime msec
no service timestamps debug datetime msec
service password-encryption
!
hostname S1_Developers
!
enable secret 5 $1$mERr$3UkiPHj9K207NKhRz7O3X.
!
!
!
ip domain-name TechNova.com
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
interface FastEthernet0/1
description Link To PC0
!
interface FastEthernet0/2
description Link To PC1
!
interface FastEthernet0/3
description Link To PC2
!
interface FastEthernet0/4
description Link To PC3
!
interface FastEthernet0/5
description Link To PC4
!
interface FastEthernet0/6
description Link To PC5
!
interface FastEthernet0/7
description Link To PC6
!
interface FastEthernet0/8
description Link To PC7
!
interface FastEthernet0/9
description Link To PC8
!
interface FastEthernet0/10
description Link To PC9
!
interface FastEthernet0/11
description Link To PC10
!
interface FastEthernet0/12
description Link To PC11
!
interface FastEthernet0/13
!
interface FastEthernet0/14
!
interface FastEthernet0/15
!
interface FastEthernet0/16
!
interface FastEthernet0/17
!
interface FastEthernet0/18
!
interface FastEthernet0/19
!
interface FastEthernet0/20
!
interface FastEthernet0/21
!
interface FastEthernet0/22
!
interface FastEthernet0/23
!
interface FastEthernet0/24
!
interface GigabitEthernet0/1
!
interface GigabitEthernet0/2
!
interface Vlan1
description link_to_R1
ip address 192.168.0.2 255.255.255.224
!
ip default-gateway 192.168.0.1
!
banner motd ^C
****************************************
** No unauthorized access beyond here **
****************************************
^C
!
!
!
line con 0
password 7 082F4358081801
login
!
line vty 0 4
password 7 08254D4F1F160B
login
transport input ssh
line vty 5 15
password 7 08254D4F1F160B
login
transport input ssh
!
!
!
!
end

```
</details>
