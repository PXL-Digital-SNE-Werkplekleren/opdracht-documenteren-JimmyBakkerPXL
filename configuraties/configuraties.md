Hier staan de configuraties van de apparaten.

<details>
<summary class="text-purple giant-text">Technova_Router</summary>

Hostname	:	Technova_Router
secret pw	:	tnadmin01
enablepw	:	novaad95	
virtual terminal password	:	daavon68	
username	:	sshuser	
 			
Domein naam	:	TechNova.com
			
ROUTER CONFIG			
			
Current configuration : 1419 bytes			
!			
version 15.4			
no service timestamps log datetime msec			
no service timestamps debug datetime msec			
service password-encryption			
security passwords min-length 8			
!			
hostname Technova_Router			
!			
login block-for 120 attempts 3 within 60			
!			
!			
enable secret 5 $1$mERr$YwhBKeInWtWvGxc1j5a1X1	
!			
!			
!			
!			
!			
!			
no ip cef			
ipv6 unicast-routing			
!			
no ipv6 cef			
!			
!			
!			
username sshuser			
!			
!			
!			
!			
!			
!			
!			
!			
!			
!			
ip domain-name TechNova.com			
!			
!			
spanning-tree mode pvst			
!			
!			
!			
!			
!			
!			
interface GigabitEthernet0/0/0			
ip address 192.168.0.33 255.255.255.240			
duplex auto			
speed auto			
ipv6 address FE80::2:1 link-local			
ipv6 address 2001:DB8:2::2/64			
!			
interface GigabitEthernet0/0/1			
description Link to S1_Developers			
ip address 192.168.0.1 255.255.255.224			
duplex auto			
speed auto			
ipv6 address FE80::1 link-local			
ipv6 address 2001:DB8:1::1/64			
!			
interface Vlan1			
no ip address			
shutdown			
!			
router rip			
!			
ip classless			
!			
ip flow-export version 9			
!			
!			
ip access-list extended sl_def_acl			
deny tcp any any eq telnet			
deny tcp any any eq www			
deny tcp any any eq 22			
permit tcp any any eq 22			
!			
banner motd ^C			
/-------------------------------------\			
|***** Authorized Personel Only *****|			
| |			
\_____________________________________/			
^C			
!			
!			
!			
!			
line con 0			
password 7 082F43580818014E47			
login			
!			
line aux 0			
!			
line vty 0 4			
exec-timeout 2 30			
password 7 08254D4F1F160B414A			
login			
transport input ssh			
line vty 5 15			
login			
!			
!			
!			
end
</details>