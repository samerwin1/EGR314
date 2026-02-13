---
title: Microcontroller Selection
tags:
- tag1
- tag2
---

## Overview
This page contains resources for and details about the selected microcontroller for the distance-sensing module.

## Specifications/Links
| PIC Info                                      | Answer |
| --------------------------------------------- | ------ |
| Model                                         | **PIC18F47K42** |
| Product Page URL                              | [Microchip](https://www.microchip.com/en-us/product/pic18f47k42_) |
| Datasheet URL(s)                              | [Datasheet](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://ww1.microchip.com/downloads/aemDocuments/documents/MCU08/ProductDocuments/DataSheets/PIC18%28L%29F26-27-45-46-47-55-56-57K42-Data-Sheet-40001919G.pdf) |
| Application Notes URL(s)                      | [Getting Started with Writing C-Code for PIC18F](https://www.microchip.com/en-us/application-notes/tb3261)<br>\* [Interfacing Serial EEPROMs with 8-Bit PIC Microcontrollers](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ApplicationNotes/AppnoteSourceCode/EXP8I2CClick.X.zip) |
| Vendor link                                   | [DigiKey](https://www.digikey.com/en/products/detail/microchip-technology/pic18f47k42-e-pt/7561732?_gl=1*1ibdds0*_up*MQ..*_gs*NA..&gclid=Cj0KCQiAyvHLBhDlARIsAHxl6xoux5zsYtU1Ezyln3WfZIBmErhYlq292bSJn2TigaG7eBxado_VPZIaAq0nEALw_wcB&gclsrc=aw.ds&gbraid=0AAAAADrbLlhhoVM0ppv4g4DBdD7niqkX3) |
| Code Examples                                 | N/A |
| External Resources URL(s)                     | [Scanning LiDAR device implemented on PIC](https://www.youtube.com/watch?v=mwJAvcA9KmY) |
| Unit cost                                     | $2.93/each |
| Supply Voltage Range                          | 2.3V/3.3V/5.5V/-0.3V ; +6.5V (Min/Nominal/Max/Absolute Max) |
| Absolute Maximum Current <br> (for entire IC) | 350 mA |
| Maximum GPIO current <br> (per pin)           | +/-50 mA |
| Supports External Interrupts?                 | Yes |
| Required Programming Hardware, Cost, URL      | [MPLAB SNAP](https://www.microchip.com/en-us/development-tool/pg164100); $10.99/each (already owned) |
| Works with MPLabX?                            | Yes |
| Works with Microchip Code Configurator?       | Yes |

## Pin Allocation
| Module | # Available | Needed | Associated Pins |
| ---------- | ----------- | ------ | ------------------------------ |
| GPIO       | 36          | 2      | RA(0-7), RB(0-7), RC(0-7), RD(0-7), RE(0-3) |
| ADC        | 35          | 0      | RA(0-7), RB(0-7), RC(0-7), RD(0-7), RE(0-2) |
| UART       | 2           | 1      | RB(6-7), RC(6-7) |
| SPI        | 1           | 0      | RA5, RC(3-4) |
| I2C        | 2           | 1      | RB(1-2), RC(3-4) |
| PWM        | 4           | 0      | RB(0,5), RC(1-2) |
| ICSP       | 1           | 1      | RB(6-7) |

## Team Role
My role on the team is to create a module which can measure the distance from the product to an object in its path, process the data, and send it to the Human-Machine Interface. I will be using a single-point ToF LiDAR serial sensor to measure the distances. The sensor will be controlled by the PIC18F47K42 microcontroller through I2C serial communication. My module will be sharing an external power source (battery) with the rest of the modules on the greater mobile unit. I will use a regulator to convert this power into a 3.3V switching power supply. My module will also be receiving data from the module directly upstream and passing it, along with the distance data, to the module directly downstream. This communication will be handled with UART serial communication. My module will not have its own display but will make use of a generic LED to signify module status.

## MPLABXIDE MCC Setup

The image below shows the setup of the Master Code Configurator inside MPLABXIDE, verifying that the chosen microcontroller can be used to power all necessary peripherals for the module.

[MCC Setup](MCCSetupTest.png)

The setup includes 2 pins for communicating with other modules through UART, 2 pins for controlling the LiDAR sensor through I2C, 1 GO pin for controlling the status-LED, and 1 GI pin for receiving a pushbutton signal(debugging). There are more than enough pins for all the functionality needed, and the MCC files have succesfully generated with no errors. This test generation is evidence that the microcontroller will be sufficient for this module's purposes.

## Final Microcontroller Choice: **PIC18F47K42**

[PIC18F47K42](PIC18F47K42(SurfaceMount).png)

After researching, collecting resources, reviewing the datasheet, reviewing pin/module-allocation, and creating a test project in MPLABXIDE, it is safe to say that the PIC18F47K42 will provide more than enough functionality for the purposes of the distance-sensing module. Not only do I have experience using the through-hole package of this microcontroller, I have also found a plethora of resources to feel comfortable using it for the project. It is low-cost, can be programmed using the SNAP tool which has already been provided, and has more than enough pins and modules. Finally, testing the setup in the MPLAB software has proven that it can be programmed for the use-case that is required.
