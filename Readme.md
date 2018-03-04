# Setting up Espruino on Nucleo F401RE (on MacOS)

## Upgrade Board Firmware

1. visit the "Getting Started" section of the product homepage: https://os.mbed.com/platforms/ST-Nucleo-F401RE/#getting-started
2. there you will find the ST-LINK/V2 firmware upgrade (Java version for all platforms)
3. before running the Java program, install libusb ```brew install libusb```
4. start the upgrader from console with ```java -jar STLinkUpgrade.jar```

## Install Espruino Firmware

1. visit Espruino download page: https://www.espruino.com/Download
2. download newest version
3. paste the espruino_xxxx_nucleof401re.bin firmware file into the boards flash drive
4. wait until LED stops blinking

## Using the Espruino Web IDE

1. install and run the Chrome extension from: https://chrome.google.com/webstore/detail/espruino-web-ide/bleoifhkdalbjfbobjackfdifdneehpo
2. connect to the board ```/dev/tty.usbmodem141```
3. load the example program and flash it onto the board

```
var  on = false;
setInterval(function() {
  on = !on;
  LED1.write(on);
}, 500);
```
