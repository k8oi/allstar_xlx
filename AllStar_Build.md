#Work in Progress! Last Update 2024-01-22
## AllStar Build
### Os Install
1. Get AllStar image for Pi: [AllStarLink RPi Images](http://downloads.allstarlink.org/ASL_Images_Beta/Raspberry_Pi2_3_4/)
1. Burn image to SD Card and install in Pi
1. User: `repeater` Pass: `allstarlink`
1. Update ASL GPG package key (all as root)
``` 
curl -s http://apt.allstarlink.org/repos/repo_signing.key | sudo apt-key add -
apt update
apt upgrade
reboot
```
### ASL Configure
1. `sudo asl-menu`
### Remote connect with Transceive app (Mac Client)
1. User `iaxclient` user
1. Change `iaxclient` password in `iax.conf`

### Configure ASL with Private Server for XLX connection
1. Edit `/etc/asterisk/rpt.conf`
  - https://s3-us-west-1.amazonaws.com/groupsioattachments/18573/21794260/3639/0?AWSAccessKeyId=AKIAJECNKOVMCCU3ATNQ&Expires=1705927633&Signature=RBGOlATvAOI82oG5sXeG7AjGVVI%3D&response-content-disposition=inline%3B+filename%3D%22ASL%2520to%2520DMR%2520Bridge.pdf%22
1. Paste the following block:
```
[1999]
rxchannel = USRP/127.0.0.1:34001:32001
duplex = 0
hangtime = 0
althangtime = 0
holdofftelem = 1
telemdefault = 0
telemdynamic = 0
linktolink = no
nounkeyct = 1
totime = 180000
idrecording = |ie
idtalkover = |ie
```

### Install DVSwitch on existing Linux Install
http://dvswitch.org/DVSwitch_install.pdf
```
wget http://dvswitch.org/buster
sudo chmod +x buster
sudo ./buster
sudo apt-get update
sudo apt-get install dvswitch-server
```
