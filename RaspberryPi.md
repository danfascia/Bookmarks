# Raspberry Pi Bits I've found useful

## Networking

### [Connecting over USB serial cable](https://www.tumfatig.net/20180701/access-raspberry-pi-3-uart-console-on-macos/)

This was actual more of a PITA than expected and the solution that finally worked for me was to establish a connection to the USB serial device (once drivers installed) then once it displayed connected, power up the Pi and watch its boot sequence. The command I used was

* **Wifi Power Management** can be a problem with Pis that depent on WLAN. It seems that after a period of inactivity they become uncontactable over external networks. Disabling wifi power management is said to help.

```iwconfig wlan0 power off```

This line can be added to `/etc/rc.local` to ensure this feature is permanent on boot

```sudo cu -l /dev/cu.usbserial -s 115200```

## Server Software
 
* [Installing NodeJS for ARM](https://thisdavej.com/beginners-guide-to-installing-node-js-on-a-raspberry-pi/) install git first
