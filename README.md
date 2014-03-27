#A library to connect arduinoYun to nodeJS via a socket.io protocol#

this library works in combination with a python script that handle the socket.io connection

you will need an arduino YUN properly configured to connected to the Internet
	
	
to configure the YUN for 802.x network like eduroam follow this guide 	[http://forum.arduino.cc/index.php?topic=197267.0](http://forum.arduino.cc/index.php?topic=197267.0)
Thanks bitfrosting
	 

##how to install the library?##

1. Connect to the Arduino Yun via ssh

```
ssh root@myYun.local
```
2. update the packages
```
opkg update
```
3. We want to install openssh-sftp-server so that we can connect to the yun via our favorite ftp software (fliezilla, cyberduck, etc) 
 
 ```
 opkg install openssh-sftp-server
 ```
 
 if it doesn't find the package you have tu update the repository list
 open the opkg configuration file
 
 ```
 vi /etc/opkg.conf
 ```
 and change the first line to
 ```
 
 src/gz barrier_breaker http://download.linino.org/dogstick/all-in-one/latest/packages/
 ```
 
 
 