# linux

### Wifi

- howto
- Set up tplink usb wifi - follow instructions here: https://askubuntu.com/questions/1334925/tp-link-archer-t3u-plus-doesnt-work  
$ sudo apt update  
$ sudo apt install build-essential git dkms bc  
$ sudo git clone "https://github.com/RinCat/RTL88x2BU-Linux-Driver.git" /usr/src/rtl88x2bu-git  
$ sudo sed -i 's/PACKAGE_VERSION="@PKGVER@"/PACKAGE_VERSION="git"/g' /usr/src/rtl88x2bu-git/dkms.conf  
$ sudo dkms add -m rtl88x2bu -v git  
$ sudo dkms autoinstall  
***Then remove, and re-insert USB wifi module and it should work

Above uses this repository: https://github.com/RinCat/RTL88x2BU-Linux-Driver

Some additional explanations here:
- [How to Install a TP-LINK Adapter on Linux Ubuntu](https://community.tp-link.com/en/home/stories/detail/323)
- [Install TP-Link AC600 Archer T2U Nano on Ubuntu](https://ostechnix.com/install-tp-link-ac600-archer-t2u-nano-wifi-usb-adapter-in-linux/)


### Some commands post-install

$ apt-get update
$ apt-get upgrade

### Change background colour

$ gsettings set org.gnome.desktop.background picture-options 'none'  
$ gsettings set org.gnome.desktop.background primary-color '#000000'  

### Install video codecs if not already installed

$ sudo add-apt-repository multiverse
$ sudo apt install ubuntu-restricted-extras

### Allow right-click for new file

$ touch ~/Templates/"Untitled Document"  (Note: can do this with all file-types)

### Change ownership of storage drive

$ chown user -R /home/user/Public  
$ sudo chown user:user /mnt/lookoverhere  
$ chown -R user:user /movies 

### Install programs

$ apt-get install gparted  

$ sudo add-apt-repository ppa:sunderme/texstudio  
$ apt-get install texstudio

yt-dlp: see https://github.com/yt-dlp/yt-dlp for info  
$ sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/bin/yt-dlp  
$ sudo chmod a+rx /usr/local/bin/yt-dlp  

# Docker install  
$ sudo apt update  
$ sudo apt upgrade  
$ sudo apt install docker.io  
$ sudo usermod -a -G docker $USER (so that there is no need to run in sudo)  

### To enable start at boot  
$ sudo systemctl start docker  
$ sudo systemctl enable docker  

### Stop and restart docker  
$ sudo systemctl stop docker  
$ sudo systemctl restart docker  

### To move install to a different drive  


### Other commands  
$ sudo docker ps (list docker containers with their IDs)  
$ docker ps -a (list all containers whether running or stopped)  
$ docker stop container_name_or_ID  
$ sudo docker cp sinegraph.jpg 17containerIDd9:/home/path/repo_images/  
$ sudo docker cp container:source_path host_destination_path  

