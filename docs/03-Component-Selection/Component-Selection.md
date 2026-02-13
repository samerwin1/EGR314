---
title: Component Selection
---

## Module's Selected Major Components

The following sections are the selected major components necessary for providing power to the distance-sensing module and meeting the module's product requirements.

### Power Management

**LM2596-3.3 Switching Regulator:** This regulator will be used to convert the external unregulated DC power source into a switching 3.3V DC power supply. This will allow the microcontroller to be powered while improving efficiency.

![](LM2596S-3.3(Regulator).png)

### Sensor

**TFLuna I2C LiDAR Module:** This ToF single-point LiDAR sensor will provide the product with the capability to measure the distance to objects in its path.

![](TFLunaI2C(LiDAR).png)

-----------

## Comparison Tables

### **Voltage Regulator**

| **Component** | **Pros** | **Cons** |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TL2575(Regulator).png)<br> TL2575-33IKTTR Switching Regulator<br>$2.58/each<br>[link to product](https://www.digikey.com/en/products/detail/texas-instruments/TL2575-33IKTTR/1629209) | \* Inexpensive<br>\* Provides required 3.3V switching output<br>\* Meets surface mount constraint of project | \* Requires external inductor, diode, capacitors<br>\* 1A output may be limiting |
| ![](LM2596S-3.3(Regulator).png)<br> LM2596-3.3 Switching Regulator<br>$1.17/each<br>[link to product](https://www.digikey.com/en/products/detail/evvo/LM2596S-3-3-EV/24370077) | \* Least expensive<br>\* Provides requred 3.3V switching output<br>\* 3A output provides extra headroom<br>\* Meets surface mount constraint of project | \* Requires external inductor, diode, capacitors<br>\* Lower efficiency |
| ![](R-78B3.3-1.5(Regulator).png)<br> R-78B3.3-1.5 Switching Regulator<br>$12.94/each<br>[link to product](https://www.digikey.com/en/products/detail/recom-power/r-78b3-3-1-5/2256231) | \* Requires no external components<br>\* Provides required 3.3V switching output<br>\* 1.5A output allows sufficient current draw | \* Very expensive<br>\* Through-hole package does not meet surface mount constraint |

**Selection:** LM2596-3.3 Switching Regulator

**Rationale:** The selected regulator meets the project and module requirements, allows the highest current draw, and is the least expensive of the three.

### **Sensor**

| **Component** | **Pros** | **Cons** |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TFMini-S(LiDAR).png)<br> TFMini-S Micro LiDAR Module<br>$72.95/each<br>[link to product](https://www.sparkfun.com/tfmini-s-micro-lidar-module.html?utm) | \* Great range<br>\* Low avg current/range ratio<br>\* Meets serial sensor constraint of project | \* Very expensive<br>\* High power consumption |
| ![](VL53L1X(LiDAR).png)<br> Pololu VL53L1X Distance Sensor<br>$22.95/each<br>[link to product](https://www.pololu.com/product/4071) | \* Least expensive<br>\* Low current/power draw<br>\* High resolution<br>\* Very lightweight | \* Short range<br>\* PWM output does not meet the serial sensor constraint of the project |
| ![](TFLunaI2C(LiDAR).png)<br> TFLuna I2C LiDAR Module<br>$24.99/each<br>[link to product](https://www.mouser.com/ProductDetail/Benewake/TF-Luna-I2C?qs=DPoM0jnrROUWvdDwJYVpzw%3D%3D&mgh=1&utm) | \* Suitable range<br>\* Within budget<br>\* Meets serial sensor constraint of project | \* Relatively expensive<br>\* Range could be lower than optimal in unideal conditions |

**Selection:** TFLuna I2C LiDAR Module

**Rationale:** While it may not be able to consistently read at the target range defined in product requirements, it should read above the threshold range. It is the best middle ground to meet the module requirements while still fitting in the project budget.
