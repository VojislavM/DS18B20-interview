# DS18B20-interview
This repository is meant for an interview task. 

## Interview task:

### Overview:
Create a simple application that will demonstrate the use of the DS18B20 temperature sensor over I2C bus using DS2482 bridge device. 
A sample needs to be created for Zephyr RTOS platform running on the nRF52832/40 (ARM Cortex M4) chip.

### Technical Overview:
Provide communication between the sensor and the MCU over the I2C to 1-wire bridge by connecting all necessary components using jumper wires.
To achieve I2C communication on the MCU side use Zephyr RTOS integrated I2C driver.
Data has to be received by using the JLink RTT (Real Time Tranfer) which can be utilized over the existing USB connection between the host machine and the development kit.
To achieve the communication on the MCU side use the Zephyr RTOS Logging library with RTT.
On the host side use the JLinkRTTViewer program.  

Every second user should receive from the sensor a temperature in the format:
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
