# Hi, I'm Ilia 👋

Software Engineer specializing in C/C++, STM32, FreeRTOS, Embedded Linux.

I build real-time systems close to the hardware: interrupt-driven firmware, sensor acquisition, hardware interfaces, network communication, concurrent Linux applications, and complete embedded prototypes.

## Technical Focus

- **Languages:** C, C++
- **Hardware Platforms:** STM32 NUCLEO-F756ZG (ARM Cortex-M7), BeagleBone Green (TI Sitara AM3358 / ARM Cortex-A8)
- **Embedded Firmware:** STM32 HAL, FreeRTOS, interrupt- and DMA-driven firmware
- **Embedded Linux:** Linux system programming, POSIX APIs, systemd
- **Sensors & Actuators:** Pimoroni ICM-20948 IMU, SG90 servo motor, 28BYJ-48 stepper motor
- **GNSS & Timing:** Quectel LC86G-LA GNSS receiver, NMEA positioning, PPS timing
- **Hardware Interfaces:** UART, SPI, I²C, ADC, DAC, GPIO, hardware timers
- **Concurrency & IPC:** POSIX threads, processes, shared memory, pipes, signals, synchronization
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, Ethernet, SQLite
- **Development Tools:** Git, GNU Make, STM32CubeIDE, STM32CubeMX, VS Code

## Featured Projects

### 🛣️ [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector)

Real-time road impact candidate detection and GNSS localization system built on STM32F756ZG and FreeRTOS.

Key features:

- Interrupt-driven ICM-20948 IMU acquisition at approximately 102 samples per second
- Quectel LC86G-LA GNSS positioning with PPS-based hardware timestamp capture
- Common TIM2 timebase for synchronizing IMU measurements with GNSS time
- Acceleration-baseline algorithm associating impact candidates with UTC timestamps and coordinates
- Real-hardware validation with documented field-test output, photographs, and video

### 🚗 [Parking System](https://github.com/IliaRakhlevski/Parking-System)

Distributed parking management system integrating STM32 firmware, BeagleBone Green, and multiple Embedded Linux applications.

Key features:

- Multi-process Linux architecture with POSIX threads and synchronization
- TCP/IP communication between embedded clients and an event-driven server
- System V shared memory, shared queues, unnamed pipes, and POSIX signals
- SQLite-based parking-session and tariff management
- STM32-to-Linux integration over I²C with automatic startup through systemd

### 🔧 [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester)

Automated hardware validation system for STM32F756ZG peripherals using FreeRTOS and a Linux UDP test server.

Key features:

- Concurrent validation of UART, SPI, I²C, ADC, DAC and timer peripherals
- Interrupt- and DMA-based test modes
- Automated PASS/FAIL evaluation with random payload generation and CRC verification
- UDP communication between the STM32 firmware and Linux server
- Runtime statistics and persistent test results stored in SQLite
