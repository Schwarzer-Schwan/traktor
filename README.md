# traktor
Traktor will autamically install Tor, privoxy, dnscrypt-proxy and Tor Browser Launcher in either a Debian based distro like Ubuntu or an Arch based distro  and configures them as well.

To do this, just run 'traktor.sh' file in a supported shell like bash and watch for prompts it asks you.

## Note
Do NOT expect anonymity using this method. Privoxy is an http proxy and can leak data. If you need anonymity or strong privacy, manually run torbrowser-launcher after installing traktor and use it.

## Install
### Ubuntu
    sudo add-apt-repository ppa:dani.behzi/traktor
    sudo apt update
    sudo apt install traktor
### ArchLinux
    yaourt -S traktor
### Other (May not be able to install yet)
    sudo apt install python-gi #(Optional, for having a graphical indicator) ## Unity & XFCE & Gnome
    sudo apt install gir1.2-appindicator3-0.1 #(Optional, for having a graphical indicator) ## Gnome
    wget https://github.com/ubuntu-ir/traktor/archive/master.zip -O traktor.zip
    unzip traktor.zip && cd traktor-master
    ./traktor.sh

## Remote update
    curl -s https://raw.githubusercontent.com/ubuntu-ir/traktor/master/traktor.sh | sh
    
## Changes
    1.6 version:
        1. fix icons tor
        2. add new obfs3 bridges
        3. add new obfs4 bridges
        4. backup torrc file
        5. add privoxy package
        6. remove polipo package
        7. change port
