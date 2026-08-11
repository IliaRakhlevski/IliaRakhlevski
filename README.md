# Hi, I'm Ilia 👋

C/C++ Software Engineer with experience in large-scale software development, system analysis, debugging, and embedded systems.

My background spans desktop and system-level software, real-time applications, and embedded development. I am currently focusing on ARM-based embedded systems, FreeRTOS, and Embedded Linux through hands-on projects involving real hardware.


## Technical Focus

- **Languages:** C, C++
- **Hardware Platforms:** STM32 NUCLEO-F756ZG (ARM Cortex-M7), BeagleBone Green (TI Sitara AM3358 / ARM Cortex-A8), FriendlyARM Mini2440 (Samsung S3C2440 / ARM9)
- **Real-Time & RTOS:** FreeRTOS, task scheduling, synchronization, inter-task communication
- **Embedded Firmware:** bare-metal ARM, STM32 HAL/CMSIS, direct memory-mapped register access, interrupt- and DMA-driven firmware
- **Embedded Linux:** Linux system programming, POSIX APIs, multi-process applications, systemd
- **Sensors & Actuators:** Pimoroni ICM-20948 IMU, Quectel LC86G-LA GNSS receiver, SG90 servo motor, 28BYJ-48 stepper motor
- **Hardware Interfaces & Control:** UART, SPI, I²C, ADC, DAC, GPIO, hardware timers, PWM
- **Concurrency & IPC:** POSIX threads, processes, mutexes, semaphores, condition variables, shared memory, pipes, signals
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, LwIP, Ethernet, SQLite
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

- Concurrent validation of UART, SPI, I²C, ADC, DAC, and timer peripherals
- Interrupt- and DMA-based test modes
- Automated PASS/FAIL evaluation with random payload generation and CRC verification
- UDP communication between the STM32 firmware and Linux server
- Runtime statistics and persistent test results stored in SQLite

### 🚨 [City Emergency Dispatch](https://github.com/IliaRakhlevski/City-Emergency-Dispatch)

Real-time emergency dispatch simulation built with FreeRTOS POSIX on Linux, featuring UDP networking, priority scheduling, SQLite persistence, and fault recovery.

Key features:

- FreeRTOS tasks, queues, mutexes, and event groups for concurrent event processing
- Priority-based dispatch to specialized departments and independent vehicle tasks
- UDP client-server communication with acknowledgements and completion reporting
- SQLite event persistence, status tracking, and runtime statistics
- Dynamic resource management, retry and fault-recovery mechanisms, validated through a continuous 10-hour stress test
