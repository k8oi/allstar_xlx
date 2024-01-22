## AllStar Build
### Os Install
1. Get AllStar image for Pi: [HamVoip RPi Images](https://hamvoip.org/#image)
1. Burn image to SD Card and install in Pi
1. ssh -p 222 root@x.x.x.x
1. Userid: root Pass: root

In /etc/asterisk/iax.conf in [general] section add:
calltokenoptional=0.0.0.0/0.0.0.0
requirecalltoken=no
