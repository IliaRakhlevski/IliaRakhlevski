# Hi, I'm Ilia 👋

C/C++ Software Engineer with a background in embedded and real-time systems.

Currently focused on modern embedded development with ARM, STM32, FreeRTOS, and Embedded Linux, combining low-level firmware, real hardware, RTOS-based systems, and Linux system programming.

## Technical Focus

- **Languages:** C, C++
- **Hardware Platforms:** STM32 NUCLEO-F756ZG (ARM Cortex-M7), BeagleBone Green (TI Sitara AM3358 / ARM Cortex-A8), FriendlyARM Mini2440 (Samsung S3C2440 / ARM9)
- **Real-Time & RTOS:** FreeRTOS, task scheduling, priority-based scheduling, queues, mutexes, semaphores, event groups, task notifications, ISR-to-task synchronization
- **Embedded Firmware:** bare-metal ARM, STM32 HAL/CMSIS, direct memory-mapped register access, interrupt- and DMA-driven firmware, peripheral configuration and control
- **Embedded Linux:** Linux system programming, POSIX APIs, multi-process applications, cross-compilation for ARM, systemd
- **Sensors & Actuators:** Pimoroni ICM-20948 IMU, SG90 servo motor, 28BYJ-48 stepper motor
- **GNSS & Timing:** Quectel LC86G-LA GNSS receiver, NMEA positioning, PPS synchronization, hardware input capture
- **Hardware Interfaces & Control:** UART, SPI, I²C, ADC, DAC, GPIO, hardware timers, PWM
- **Concurrency & IPC:** POSIX threads, processes, mutexes, semaphores, condition variables, System V shared memory, shared queues, pipes, signals
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, event-driven networking (`select()`), Ethernet, SQLite
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
