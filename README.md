# myrpi

1. preparation
Download image https://www.raspberrypi.org/downloads/
Write image to MircoSD Card with: https://etcher.io/

2. system setup
# change passwords
sudo passwd root
sudo passwd pi
# enable ssh
run: nano /etc/ssh/sshd_config
run: service ssh restart

# raspi-config 
run: raspi-config
- expand filesystem
- enable SSH
- enable SPI


3. install spidev

# update system
sudo apt-get update
sudo apt-get upgrade
# install python and spidev
sudo apt-get install python-dev python3-dev
cd ~
git clone https://github.com/doceme/py-spidev.git
cd py-spidev
make
sudo make install
