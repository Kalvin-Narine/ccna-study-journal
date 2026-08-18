MAXIMUM HOSTS PER NETWORK

192.168.1.0/24
(Class C network) 

The last 8 bits are the host portion
32-24=8

The host portion can be 192.168.1.0.24-192.168.1.255/25

(gives a range of 0 ---> 255)

The host portion= 8 bits 2^8=256

Power of 8 because there are 8 bits

If the host portion is all 0s = network address(Network id)
It can't be assigned to a host 
If the host portion is all 1s= broadcast address, 
Can be assigned to a host 

Maximum hosts per network 2^8-2=254 

Subtract 2 which represents the network address and broadcast address. 


CLASS B NETWORK 

172.16.0.0/16 → 172.16.255.255/16
Host portion = 16 bits = 2^16 =65536
Maximum hosts per network = 2^16-2 = 65,534 hosts


CLASS A NETWORK


10.0.0.0/8 —> 10.255.255.255/8
Host portion = 24 bits = 2^24 = 16777216 hosts 
Maximum hosts per network = 2^24-2= 16777214


To find maximum hosts per network it is 2^n-2 
n= number of hosts bits. 


FIRST/LAST USABLE ADDRESS
—----------------------------------------------------------------------------------------------------------------------------

Class C address

192.168.1.0/24 → 192.168.1.255/24
Network ^^^		Broadcast^^^


Add 1 by changing the last bit of the host portion to one 
00000000
00000001

192.168.1.1/24= first usable

Add one to the network address and we get the first usable address. 

Last usable address
Switch the last bit to  a 0 
11111111
11111110

192.168.1.254= last usable address


We just subtract one from the broadcast address. 
—----------------------------------------------------------------------------------------------------------------------------
CLASS B address

172.16.0.0/16 (NETWORK ADDRESS) → 172.16.255.255/16 (BROADCAST ADDRESS)

172.16.0.0/16 (NETWORK ADDRESS)

Add 1 to Host portion so 0000 0000 0000 0001

172.16.0.1/16 =FIRST USABLE ADDRESS


172.16.255.255/16 (BROADCAST ADDRESS)

Subtract 1 to Broadcast Address so 1111 1111 1111 1110

172.16.255.254/16 =LAST USABLE ADDRESS

—----------------------------------------------------------------------------------------------------------------------------
CLASS A ADDRESS

10.0.0.0/8(NETWORK ADDRESS) → 10.255.255.255/8( BROADCAST ADDRESS)


10.0.0.0/8(NETWORK ADDRESS)
Add 1 to Host portion so 00000000.00000000.0000001

10.0.0.1 /8= first usable

10.255.255.255/8( BROADCAST ADDRESS)

Subtract 1 from broadcast address

11111111.11111111.11111110
10.255.255.254/8= last usable 



IPV4 ADDRESSING




CISCO CLI

R1>enable (enters privileged exec mode
R1#show ip interface brief 
Lists the Interfaces, IP Addresses, Method, Status, and Protocol

Interfaces:
What port interfaces are available/connected
IP Addresses:
What IP Address is assigned.
Method:
What method was the IP address assigned?
Status (Layer 1 Status)
Current status of interface
'administratively down' : Interface has been disabled with the 'shutdown' command
Administratively down is the DEFAULT status of Cisco Router interfaces.
Router: Administratively down is default
Switch: Administratively down is NOT default
They will either be up if connected to another device or down if they are not 

Cisco Switch interfaces are NOT administratively down by DEFAULT.


Protocol:
Layer 2 status 
Cannot operate if Status (Layer 1) is down
You will never see an interface with a down in the status column and an up in the protocol column. The reverse is possible






R1# configure terminal (enters global configuration mode)
R1(config)#interface gigabitethernet 0/0 
(This can be shortened to 'g0/0' like they are listed in physical network maps.)

R1(config-if)#


This sets the IP ADDRESS and SUBNET MASK of device
R1(config-if) #ip address 10.255.255.254 255.0.0.0

 This enables the device

R1(config-if) #no shutdown

Now that we used the no shutdown command Two messages should appear showing the state has changed to 'up' (Status). Second message should show line protocol is now 'up' (Protocol).

'do' allows you to run a Privileged EXEC command from outside the mode.

R1(config-if) #do show ip interface brief








____________________________________________________________________________
'show interfaces ' {interface] 
Example:
R1# show interfaces g0/0 
Shows Layer 1 and Layer 2 information about the interface and some Layer 3.
Shows MAC Address (or BIA (burned in address) address)
IP Address
and so much more
'show interfaces description'

Allows you to add descriptions for interfaces.
Shows interface, status and protocol column as well 
Example:

// Configure mode for interface Gigabyte Interface 0/0

R1(config) #int g0/0

R1(config) #description ## to SW1 ##

This sets the 'Description' column to display:

Interface Description

Gi0/0 ## to SW1 ##



Its description followed by the description the ## is optional. 
