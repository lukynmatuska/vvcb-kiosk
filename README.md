# VVCB Kiosk

## Prerequisites

1. Installed [Raspberry Pi OS](https://www.raspberrypi.com/software/)
1. Enabled desktop environment with autologon

## Installation

There are basic instructions.

1. Clone this repository and enter its folder
1. Create directory for autostart
1. Copy Desktop config file to autostart folder
1. Reboot system to test it

```sh
cd ~
git clone https://github.com/lukynmatuska/vvcb-kiosk.git 
cd ~/vvcb-kiosk
mkdir -p ~/.config/autostart
ln -s ~/vvcb-kiosk/vvcb-kiosk.desktop ~/.config/autostart/vvcb-kiosk.desktop
sudo systemctl reboot
```

### Optionaly

Disable:

- screensaver
- wallpaper
