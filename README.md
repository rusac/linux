# linux

### Wifi

- howto

### Some commands post-install

$ apt-get update
$ apt-get upgrade

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
$ apt-get install texstudio
