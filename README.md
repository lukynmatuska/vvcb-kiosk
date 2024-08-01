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

### Optionally

#### Enable VNC Server

Remote desktop is very usefull, when you have no keyboard and mouse connected to kiosk.

```sh
sudo raspi-config nonint do_vnc 0
```

#### Disable screensaver

More info see in [docs](https://www.raspberrypi.com/documentation/computers/configuration.html#screen-blanking-2).

```sh
sudo raspi-config nonint do_blanking 1
```

#### Enable autologin

Boot to desktop, logging in automatically.

```sh
sudo raspi-config nonint do_boot_behaviour B4
```

#### Disable splash screen

It is better to have the splash screen off for easier problem diagnosis.

```sh
sudo raspi-config nonint do_boot_splash 1
```

## Update

All you need to update is pull the git repository.

```sh
cd ~/vvcb-kiosk && git pull
```
