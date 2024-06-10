+++
title = 'Install Openbox'
date = 2024-06-10T08:48:50Z
image = 'termux2.jpg'
+++

# install openbox on termux 

# langkah pertama 

# update termux dulu 

apt update -y

# lalu install Openbox & tigervnc

apt install openbox tigervnc dbus

# dan install nitrogen untuk set wallpaper

apt install nitrogen thunar

# lalu setting vnc 

mkdir -p ~/.vnc

echo "#!/bin/bash

[ -r ~/.Xresources ] && xrdb ~/.Xresources

export PULSE_SERVER=127.0.0.1

export DISPLAY=:1

XAUTHORITY=~/.Xauthority

export XAUTHORITY

openbox-session" > ~/.vnc/xstartup

chmod +x ~/.vnc/xstartup

wget https://raw.githubusercontent.com/Mobile-Linux-Official/Dotconfig/main/vncserver-start -O /usr/local/bin/vncserver-start

wget https://raw.githubusercontent.com/Mobile-Linux-Official/Dotconfig/main/vncserver-stop -O /usr/local/bin/vncserver-stop

chmod +x /usr/local/bin/vncserver-start

chmod +x /usr/local/bin/vncserver-stop


# Selesai instalasinya

# Sekian terima kasih 



