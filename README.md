# VVCB Kiosk

## Installation

There are basic instructions.
1. Clone this repository and enter its folder
1. Create directory for autostart
1. Copy Desktop config file to autostart folder
1. Reboot system to test it

```sh
git clone https://github.com/lukynmatuska/vvcb-kiosk.git 
cd vvcb-kiosk
mkdir -p .config/autostart
cp vvcb-kiosk.desktop .config/autostart/
sudo systemctl reboot
```

### Optionaly

Disable screensaver.
