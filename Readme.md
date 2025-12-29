<span class="text-purple giant-text">Technova Repository</span>

Op deze pagina staan de 2 configuraties die wij dienden te uploaden. 
De .cfg files zijn op deze pagina geupload en zullen kadergewijs worden weergegeven.

CONFIGURATIES TECHNOVA OPDRACHT:

ROUTER:

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

**********************************************************************

Configuratie Switch 1

Hostname	:	S1_Developers	
secret pw	:	tnadmin		
enablepw	:	novaad		
virtual terminal password	:	daavon		
username	:	sshuser		
 				
Domein naam	:	TechNova.com	
				
S1 Config				
				
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

Einde