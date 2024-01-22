## AllStar Build
### Os Install
1. Get AllStar image for Pi: [HamVoip RPi Images](https://hamvoip.org/#image)
1. Burn image to SD Card and install in Pi
1. ssh -p 222 root@x.x.x.x
1. Userid: root Pass: root

In /etc/asterisk/iax.conf in [general] section add:
calltokenoptional=0.0.0.0/0.0.0.0
requirecalltoken=no
### HamVoIP 1.7
https://transceive.app/help/node-connections#hamvoip-1.7
HamVoIP latest node software version 1.7 contains changes affecting IAX client applications such as Transceive. In order for Transceive to continue to connect to the node, the following configuration needs to be added:

1. In the client configuration section of `/etc/asterisk/iax.conf`

    [user_name]
    requirecalltoken=no

1. In `/etc/asterisk/rpt.conf`

    propagate_dtmf=yes
    propagate_phonedtmf=yes
    remote_dtmf_allowed=1

Restart the node after you modify the configuration.
