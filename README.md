# chuckcharlie/cups-avahi-airprint

Fork from [quadportnick/docker-cups-airprint](https://github.com/quadportnick/docker-cups-airprint)
chuckcharlie/cups-avahi-airprint:latest基础上增加了HP MFP 1188的驱动
https://hub.docker.com/r/jwchenzju/cups-air

docker run -d --name cups
--log-driver local
--restart unless-stopped
--network macvlan
--ip 192.168.2.25
--device=/dev/bus/usb:/dev/bus/usb
-e CUPSADMIN="print"
-e CUPSPASSWORD="print"
-e TZ="Asia/Shanghai"
-e AVAHI_HOSTNAME="cups-airprint"
jwchenzju/cups-air:1.0
