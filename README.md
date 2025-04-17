![Devide](https://raw.githubusercontent.com/ASKI-001/FALCONETTE/refs/heads/main/Images/device3.JPG)
## FALCONETTE
FALCONETTE is an free and open-source project. It disrupts various devices using an ESP32 and nRF24 modules, causing plenty of noise and sending unnecessary packets (DoS).

It interrupts whole **2.4GHz** broadband! Everything that works on 2.4GHz is being interfered, like:        
- *Bluetooth devices*
- *microphones on 2.4GHz*
- *smartphone connections (2GHz)*
- *WiFi*
- *RC Drones*
- *IoT devices*
- *wireless keyboard & mouse*
just anything on 2.4GHz!

**Remember that jamming is illegal and should not be used with malicious intent!**

**Required:** 

- ESP32 WROOM 32U
- nRF24L01+PA+LNA  (2x)
- 10uF Capacitor
- jumpers

**Aditional**
- ESP32 Expansion Board
- 10uf capacitor (2X)

## Operation Channels

- **Bluetooth** = 79CH  
  Frequency Range: 2.402 GHz to 2.480 GHz  
  Channel Width: 1 MHz


- **BLE** = 40CH  
  Frequency Range: 2.400 GHz to 2.4835 GHz  
  Channel Width: 2 MHz

- **WiFi** = 14CH  
  Frequency Range: 2.400 GHz to 2.4835 GHz  
  Channel Width: Typically 20 MHz, but can be 22 MHz or 40 MHz in some cases

- **RC drones, etc.** = 1-125CH  
  Frequency Range: 2.400 GHz to 2.525 GHz  
  Channel Width: 1 MHz

## ESP32 + nRF24L01 pinout
Two nRF24L01 modules are use for both HSPI and VSPI

### HSPI
| 1st nRF24L01 module Pin | HSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) capacitor |
| GND           | GND              | (-) capacitor |
| CE            | GPIO 16          |
| CSN           | GPIO 15          |
| SCK           | GPIO 14          |
| MOSI          | GPIO 13          |
| MISO          | GPIO 12          |
| IRQ           |                  |

### VSPI 
| 2nd nRF24L01 module Pin | VSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) capacitor |
| GND           | GND              | (-) capacitor |
| CE            | GPIO 22          |
| CSN           | GPIO 21          |
| SCK           | GPIO 18          |
| MOSI          | GPIO 23          |
| MISO          | GPIO 19          |
| IRQ           |                  |

## WIRING DIAGRAM

![Wiring](https://raw.githubusercontent.com/ASKI-001/FALCONETTE/refs/heads/main/Images/Pin.jpg)

### NRF24L01 PINS
![Pins](https://howtomechatronics.com/wp-content/uploads/2017/02/NRF24L01-Pinout-NRF24L01-PA-LNA-.png)

 ## UPLOADING CODE TO ESP32
- we upload the code using the `WEBFLASHER` tool developed by [Smoochee](https://github.com/smoochiee/). He/She or They are the real owners of this project. 

   - [WEBFLASHER](https://smoochiee.github.io/Bluetooth-jammer-esp32/flash1)
