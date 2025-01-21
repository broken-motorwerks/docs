# PCB Design
## Checklist
- [x] Power Supply
- [ ] MCU
	- [x] Decoupling caps
	- [x] Crystal
	- [x] Debug
	- [ ] Boot and Reset switches
- [x] XBEE
- [x] CAN Transceiver
- [ ] GPS
- [ ] IMU
## JLCPCB Notes
- Better component search: <https://yaqwsx.github.io/jlcparts/#/>
### Easyeda2kicad
- Permits importing symbol and footprint, e.g.
```
(easyeda) ➜ easyeda2kicad --full --lcsc_id=C5219261
```
- Just need to find the `lcsc_id`, which so far seems to be the JLCPCB part number on their site
## Components
### Power Supply
- TI LMR51430 (1.1 Mhz)
- [data sheet](https://www.ti.com/lit/ds/symlink/lmr51430.pdf?ts=1734408447187&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLMR51430%253FHQS%253Dds-SNVS107-LMR51430-feat-pf-en)
- Currently using the LMR51430 at the higher 1.1 Mhz switching frequency
### XBEE
- [XBee-PRO 900HP](https://www.digi.com/products/models/xbp9b-dpst-001)
- [User Guide](https://www.digi.com/resources/documentation/digidocs/pdfs/90002173.pdf)
- https://www.digi.com/resources/documentation/digidocs/pdfs/90002173.pdf
- Decoupling caps:
	1. 47 pf
	2. 1 µF
	3. 10 µF
### CAN Transceiver
- SN65HVD230
- [Data Sheet](https://files.waveshare.com/upload/3/3a/SN65HVD230-CAN-Board-Datasheets.pdf)
- [SN65HVD230 CAN Board Accessory board used for connecting MCUs to the CAN network, 3.3V, ESD protection](https://www.waveshare.com/sn65hvd230-can-board.htm)
### STM32
- [Getting started with STM32F3 series hardware development ](https://www.st.com/resource/en/application_note/an4206-getting-started-with-stm32f3-series-hardware-development-stmicroelectronics.pdf)
- [USB Hardware](https://www.st.com/resource/en/application_note/an4879-introduction-to-usb-hardware-and-pcb-guidelines-using-stm32-mcus-stmicroelectronics.pdf)
- [Reference Manual](https://www.st.com/resource/en/reference_manual/rm0316-stm32f303xbcde-stm32f303x68-stm32f328x8-stm32f358xc-stm32f398xe-advanced-armbased-mcus-stmicroelectronics.pdf)
- Using standard 10 pin arm cortex debug port
### LEDS
- Using [KT-0603R](https://jlcpcb.com/partdetail/Hubei_KentoElec-KT0603R/C2286)
- At 15mA, forward voltage is 2v based on chart in datasheet
- Calculating current limiting resistor:
\\[ \frac{(VCC - VF)}{I} = R \\]
\\[ \frac{(3.3\ v - 2\ v)}{0.015 \ a} = 86\ \Omega \\]
### GPS
- [SparkFun GPS Breakout - NEO-M9N, SMA](https://www.sparkfun.com/products/17285)
- [GNSS L1/L2 Multi-Band Magnetic Mount Antenna - 5m (SMA)](https://www.sparkfun.com/products/15192)