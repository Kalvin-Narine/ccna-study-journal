CLI- Command Line Interface 
The interface you use to configure cisco devices 
GUI -> (Graphical User Interface) 
Connecting to the CLI uses the console port
RJ45 and USB Mini-B are 2 of the ports on the Cisco Catalyst switch
Console cables are blue- rollover cable 
8 pins on each end 
You access the CLI after plugging in with a terminal emulator such as (PuTTy)
Use serial,adn go to open and you can connect to the CLI


^^ Cisco defaults 
They should already be set up you never really have to change them. 
The speed is 9600 bits per second
8 data bits 
1 stop bit 
No parity 
No flow control

User EXEC mode is seen as the >
Very limited 
Look at things but can't change any configuration
Also called user mode
Enable command allows you to go into Privileged EXEC Mode seen as the #
Can't change anything ib the running configuration 
Can turn off the switch 
Provides complete access to view the device's configuration, restart the device 
Cannot change the configuration, but can change the time on the device, save the configuration file, etc 

Global Configuration mode 
Command: configure terminal 
Seen as (config)#

Creating a password 
(config) #enable password  ?
(config) # enable password CCNA?
<cr> means no other options, so enter means that it will set

Passwords are case-sensitive
Bad secrets- incorrect password (if you type it incorrectly 3 times) 

Running-config / startup-config

These are two separate configuration files kept on the device at once
Running-config= the current, active configuration file on the device. As you enter commands in the CLI, you edit the active configuration 
startup-config= the configuration file that will be loaded upon startup of device,


#Show running-config 
Shows the running configuration

#show startup-config
Shows startup config

Everything that is saved  is shown here


Saving configuration

#write
#write memory
#copy running-config startup-config

Service password-encryption
(config) #service password-encryption

This encrypts the password in the running config

It shows the password type, such as 7, which is Cisco's proprietary service password-encryption

Enable secret is the better command it is more secure and has better encryption 

(config) #enable secret Cisco
5 in front of the password is MD5 encryption 

Always use enable secret.

Use do in front of the command to do privilege exect mode commands in other configuration levels. 

Typing no in front of the command deletes/cancel the command. 






Modes:
>  = User EXEC
#  = Privileged EXEC
(config)# = Global Configuration

Commands:
enable                -> User EXEC → Privileged EXEC
disable               -> Privileged EXEC → User EXEC
configure terminal    -> Privileged EXEC → Global Config
exit                  -> Go back one level
end or Ctrl+Z         -> Return to Privileged EXEC


Tab = auto-complete commands
? = context-sensitive help
Up Arrow = previous command



