---
title: Appendix - Controller Table for the PIC
---

| PIC Info                                      | Answer |
| --------------------------------------------- | ------ |
| Model                                         | PIC18F47K42 |
| Product Page URL                              | [Microchip](https://www.microchip.com/en-us/product/pic18f47k42_) |
| Datasheet URL(s)                              | [Datasheet](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18%28L%29F26-27-45-46-47-55-56-57K42-Data-Sheet-40001919G.pdf) |
| Application Notes URL(s)                      | [Getting Started with Writing C-Code for PIC18F](https://www.microchip.com/en-us/application-notes/tb3261)<br>\* [Interfacing Serial EEPROMs with 8-Bit PIC Microcontrollers](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ApplicationNotes/AppnoteSourceCode/EXP8I2CClick.X.zip) |
| Vendor link                                   | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/pic18f47k42-e-pt/7561732?_gl=1*1ibdds0*_up*MQ..*_gs*NA..&gclid=Cj0KCQiAyvHLBhDlARIsAHxl6xoux5zsYtU1Ezyln3WfZIBmErhYlq292bSJn2TigaG7eBxado_VPZIaAq0nEALw_wcB&gclsrc=aw.ds&gbraid=0AAAAADrbLlhhoVM0ppv4g4DBdD7niqkX3) |
| Code Examples                                 | ?      | url(s) for libraries on github or other sites related to the microcontroller and your planned peripherals |
| External Resources URL(s)                     | [Scanning LiDAR device implemented on PIC](https://www.youtube.com/watch?v=mwJAvcA9KmY) |
| Unit cost                                     | $2.93/each |
| Supply Voltage Range                          | 2.3V/3.3V/5.5V/-0.3V ; +6.5V (Min/Nominal/Max/Absolute Max) |
| Absolute Maximum Current <br> (for entire IC) | 350 mA |
| Maximum GPIO current <br> (per pin)           | +/-50 mA |
| Supports External Interrupts?                 | Yes |
| Required Programming Hardware, Cost, URL      | [MPLAB SNAP](https://www.microchip.com/en-us/development-tool/pg164100); $10.99/each (already owned) |
| Works with MPLabX?                            | Yes |
| Works with Microchip Code Configurator?       | Yes | Can be validated in MPLabX.  Screenshot required.                                                         |


| Module | # Available | Needed | Associated Pins |
| ---------- | ----------- | ------ | ------------------------------ |
| GPIO       | 36          | 2      | RA(0-7), RB(0-7), RC(0-7), RD(0-7), RE(0-3) |
| ADC        | 35          | 0      | RA(0-7), RB(0-7), RC(0-7), RD(0-7), RE(0-2) |
| UART       | 2           | 1      | RB(6-7), RC(6-7) |
| SPI        | 1           | 0      | RA5, RC(3-4) |
| I2C        | 2           | 1      | RB(1-2), RC(3-4) |
| PWM        | 4           | 0      | RB(0,5), RC(1-2) |
| ICSP       | 1           | 1      | RB(6-7) |

