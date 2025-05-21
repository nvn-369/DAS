# DAS
DATA ACQUISITION SYSTEM USING ARM7 LPC2129
# DATA ACQUISITION SYSTEM (DAS) USING LPC2129

A real-time embedded system designed to acquire, process, and transmit sensor data using the ARM7-based LPC2129 microcontroller. This project showcases seamless integration of hardware and software components for accurate and efficient environmental monitoring, making it ideal for applications in automation, healthcare, and smart agriculture.

---

## 📌 Project Overview

The **Data Acquisition System (DAS)** collects data from multiple sensors including:

- 🌡️ **Temperature sensor (LM35)**  
- 💡 **Light sensor (LDR via MCP3204 ADC)**  
- 🎛️ **Potentiometer (for voltage sensing)**  
- ⏱️ **RTC module (DS1307)** for timestamping  

These inputs are digitized using onboard and external ADCs, then displayed on a 16×2 LCD screen and simultaneously transmitted to a PC terminal via UART. The system is optimized for real-time performance and designed to be modular for future enhancements.

---

## Features

- ✅ Real-time sensor data acquisition and monitoring
- ✅ Timestamped data logging using I2C-based RTC
- ✅ SPI-based communication with external ADC (MCP3204)
- ✅ UART-based serial communication to PC
- ✅ LCD display for local visualization of live data
- ✅ Compact, scalable design for embedded and IoT applications

---

## Working Principle

Upon powering up the system, the LPC2129 microcontroller initializes all peripherals—ADC, I2C, SPI, UART, and LCD. The real-time clock (RTC) provides current time data through the I2C interface, which is stored and used for timestamping each data reading.

- The **LM35 temperature sensor** and **potentiometer** are directly connected to the internal ADC channels.
- The **LDR** is connected through the **MCP3204 external ADC** via the SPI interface.
- All sensor values are continuously sampled, converted, and formatted.
- The **LCD** displays current time, temperature (°C), potentiometer voltage (V), and light intensity (%).
- In parallel, all data is transmitted over **UART** to a PC terminal, allowing for real-time remote monitoring and data logging.

The system cycles this process in a loop, providing a live, time-stamped feed of environmental parameters.



##  Future Enhancements

- Integration with wireless modules (ESP32/Bluetooth) for remote IoT logging.
- Data storage via SD card or EEPROM.
- Web dashboard for remote visualization.
- Sensor threshold alerts and automation triggers.

---

**Developed by:**  
**Naveen S Menon**  
V24BE3N4 | Embedded Systems Engineer  
