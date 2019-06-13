# Raspberry Pi Bits I've found useful

## Networking

###[Connecting over USB serial cable](https://www.tumfatig.net/20180701/access-raspberry-pi-3-uart-console-on-macos/)### 

This was actual more of a PITA than expected and the solution that finally worked for me was to establish a connection to the USB serial device (once drivers installed) then once it displayed connected, power up the Pi and watch its boot sequence. The command I used was 

```sudo cu -l /dev/cu.usbserial -s 115200```
