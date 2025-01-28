# XBEE Notes
- XBee PRO 900HP 10K
- Family: XBP9B-DP
## UART Connection
	- Orange (TX) connected to pin 3 (DIN)
	- Yellow (RX) connected to pin 2 (DOUT)
- Radios are configured at 115200 for serial interface
## XCTU
- Configuration tool for changing radio parameters
- [User Guide](https://www.digi.com/resources/documentation/digidocs/90001458-13/default.htm#concept/c_90001458-13_start.htm?TocPath=_____1)
## Interface Notes
- SPI only operates in API mode
- Sticking with transparent mode for now as it's easier
## Configuration
### Destination addressing
- `SH` and `SL` define a device serial number
- they correspond to `DH` and `DL` on the transmitter
# Breadboard
- Base station could use a RPI 400
- Pins
	- 1 - 3.3V
	- 6 - Ground
	- 15 - TxD
	- 16 - RxD
- <https://www.pi4j.com/1.3/pins/rpi-400.html>
- XBEE power: 215 mA typical, (290 mA max)
- Looks like the 3.3v rail is capable of  providing enough power per this [stackoverflow post](https://raspberrypi.stackexchange.com/questions/51615/raspberry-pi-power-limitations):
> The Pi 3.3 V rail is widely assumed to provide 50 mA, but this is not officially documented for recent Pi models. The original Pi has an on-board linear regulator which was limited, but the B+ and later have a switch mode regulator which can supply more. The regulator chip (which supplies both 3.3 V and 1.8 V) is rated at 1 A. The MxL7704 PMIC used in the Pi3B+, Pi3A+ and Pi4 is rated at 1.5 A.
>
> [Tests](https://raspberrypise.tumblr.com/post/144555785379/exploring-the-33v-power-rail) by a member indicate up to 800 mA can be used - subject to an adequate power supply.
>
> [Electrical Specifications of GPIO](http://raspberrypi.stackexchange.com/questions/60218/what-are-the-electrical-specifications-of-gpio-pins/60219#60219) for best estimates of GPIO limits.
- Does the xbee provide any power diagnostics? Using the 3.3v rail looks okay but could be a source of degraded performance