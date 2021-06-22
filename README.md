# DS18B20-interview
This repository is meant for an interview task. 

## Interview task:

### Overview:
Create simple application that will demonstrate use of DS18B20 temperature sensor over I2C bus using DS2482 brigde device. Sample need to be created for Zephyr RTOS platform running on the nRF52832/40 (ARM Cortex M4) chip.

### Technical Overview:
Provide communication between sensor and MCU over the I2C to 1-wire bridge by connecting all necesery commponents using jumper wires. To achive I2C communication on the MCU side use Zephyr RTOS integrated I2C driver. The user will receive the data using JLink RTT (Real Time Tranfer) that can be utilized over existing USB connection between host maschine and Development kit. To achive communication on MCU side use Zephyr RTOS Logging library with RTT and on the host side use JLinkRTTViewer.  

Every seond user should receive information from sensor temperature in format:
* `DS18B20-interview: temperature = %f C\n` where `%f` represents temperature as a float value.  

### Goal:
* provide DS18B20 sensor driver API with functions:
  * `void ds18b20_init(void)`
  * `float ds18b20_read_temp(void);`
* provide sample application that utilize sensor driver and Zephyr RTOS Logging module for printing data
* provide documentation page inside this repository in Markdown format describing:
  * hardware setup
  * driver API
  * sample application

### Project components:
* **hardware (will be provided):**
  * [nRF52832/40 Development kit](https://www.nordicsemi.com/Software-and-Tools/Development-Kits/nRF52-DK)
  * USB cable
  * jumper wires
  * [mikroe I2C 1-Wire click](https://www.mikroe.com/i2c-1-wire-click)
  * DS18B20 temperature sensor

* **software components:**
  * [NCS (Nordic Connect SDK)](https://www.nordicsemi.com/Software-and-tools/Software/nRF-Connect-SDK) version = 1.5.0
  * [JLink Software](https://www.segger.com/downloads/jlink/)


