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
