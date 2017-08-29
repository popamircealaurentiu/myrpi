# myrpi

# 1. preparation
Download image https://www.raspberrypi.org/downloads/
Write image to MircoSD Card with: https://etcher.io/

# 2. system setup
# 2.1 change passwords
sudo passwd root
sudo passwd pi
# 2.2 enable ssh
run: nano /etc/ssh/sshd_config
run: service ssh restart

# 2.3 raspi-config 
run: raspi-config
- expand filesystem
- enable SSH
- enable SPI


# 3. install spidev

# 3.1 update system
sudo apt-get update
sudo apt-get upgrade
# 3.2 install python and spidev
sudo apt-get install python-dev python3-dev &&
cd ~ &&
git clone https://github.com/doceme/py-spidev.git &&
cd py-spidev &&
make &&
sudo make install
