## AllStar Build
### Os Install
1. Get AllStar image for Pi: [AllStarLink RPi Images](http://downloads.allstarlink.org/ASL_Images_Beta/Raspberry_Pi2_3_4/)
1. Burn image to SD Card and install in Pi
1. User: `repeater` Pass: `allstarlink`
1. Update ASL GPG package key
```
curl -s http://apt.allstarlink.org/repos/repo_signing.key 12 | sudo apt-key add -
sudo apt update
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
