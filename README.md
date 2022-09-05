# snapcraft
```
wget https://github.com/wongasley/fresh-linux-install/blob/main/update.sh
sudo mv /etc/apt/preferences.d/nosnap.pref ~/Documents/nosnap.backup
sudo apt update -y
sudo apt upgrade -y
sudo apt install git -y
sudo apt install zip unzip
sudo apt install git dkms -y
git clone https://github.com/aircrack-ng/rtl8812au.git
cd rtl8812au
sudo make dkms_install
sudo apt-get install python3 python3-venv python3-pip -y
sudo apt install snapd -y
sudo snap install bitwarden
sudo snap install krita
sudo snap install code --classic
sudo snap install gimp
sudo snap install spotify
sudo snap install telegram-desktop
sudo snap install brave
sudo snap install shotcut --classic
sudo snap install obs-studio
sudo snap install blender --classic
sudo snap install qbittorrent-arnatious
sudo snap install shotcut --classic
sudo snap install discord
sudo snap install node --channel=latest/edge --classic
sudo apt install vlc -y
git clone https://github.com/cilynx/rtl88x2bu.git
cd rtl88x2bu
VER=$(sed -n 's/\PACKAGE_VERSION="\(.*\)"/\1/p' dkms.conf)
sudo rsync -rvhP ./ /usr/src/rtl88x2bu-${VER}
sudo dkms add -m rtl88x2bu -v ${VER}
sudo dkms build -m rtl88x2bu -v ${VER}
sudo dkms install -m rtl88x2bu -v ${VER}
sudo modprobe 88x2bu
```
