# PCB Design
## Components
- [SparkFun GPS Breakout - NEO-M9N, SMA](https://www.sparkfun.com/products/17285)
- [GNSS L1/L2 Multi-Band Magnetic Mount Antenna - 5m (SMA)](https://www.sparkfun.com/products/15192)
- [STM32F3DISCOVERY - Discovery kit with STM32F303VC MCU - STMicroelectronics](https://www.st.com/en/evaluation-tools/stm32f3discovery.html)
- [SN65HVD230 CAN Board Accessory board used for connecting MCUs to the CAN network, 3.3V, ESD protection](https://www.waveshare.com/sn65hvd230-can-board.htm)
## PCB Notes
### JLCPCB Notes
- Better component search: https://yaqwsx.github.io/jlcparts/#/
#### Easyeda2kicad
- Permits importing symbol and footprint, e.g.
```
(easyeda) ➜  easyeda_test easyeda2kicad --full --lcsc_id=C5219261
```
- Just need to find the `lcsc_id`, which so far seems to be the JLCPCB part number on their site
### Power Supply
- https://wmsc.lcsc.com/wmsc/upload/file/pdf/v2/lcsc/2302220300_Texas-Instruments-LMR51430YFDDCR_C5219261.pdf
- https://www.ti.com/lit/ds/symlink/lmr51430.pdf?ts=1734408447187&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FLMR51430%253FHQS%253Dds-SNVS107-LMR51430-feat-pf-en
- Currently using the LMR51430 at the higher 1.1 Mhz switching frequency
## STM32
- [Getting started with STM32F3 series hardware development ](https://www.st.com/resource/en/application_note/an4206-getting-started-with-stm32f3-series-hardware-development-stmicroelectronics.pdf)
- [USB Hardware](https://www.st.com/resource/en/application_note/an4879-introduction-to-usb-hardware-and-pcb-guidelines-using-stm32-mcus-stmicroelectronics.pdf)
- [Reference Manual](https://www.st.com/resource/en/reference_manual/rm0316-stm32f303xbcde-stm32f303x68-stm32f328x8-stm32f358xc-stm32f398xe-advanced-armbased-mcus-stmicroelectronics.pdf)