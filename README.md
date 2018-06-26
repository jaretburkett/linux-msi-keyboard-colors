## Linux MSI Keyboard Colors

A simple command line application to set the keyboard colors for your msi keyboard.

## Setup

**IMPORTANT**: You need to add your user to the dialout group to access the usb device for the colors, otherwise, 
you will have to run this with 'sudo'. Run the following to add your user to the dialout group. Then restart. 

```bash
sudo cp 99-msi-keyboard.rules /etc/udev/rules.d/
sudo reload udev
sudo udevadm control --reload-rules
sudo udevadm trigger
sudo usermod -a -G dialout $USER
sudo reboot
```
