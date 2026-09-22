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

### 🚢 [Sea Battle](https://github.com/IliaRakhlevski/Sea-Battle)

Battleship in C++17 with the classic 10-ship rules (ships may not touch, a hit earns another shot), designed as a reusable game-rules library with a separate console front end.

Key features:

- Rules library with no I/O: board, fleet placement, shooting and game session are independent of the UI
- Pluggable placement and targeting strategies (Strategy), game events for any front end (Observer), dependency injection via `std::unique_ptr`
- Modern C++17: `std::optional`, `std::variant`, RAII, value types, `[[nodiscard]]`
- Computer strategies compared by measurement on simulated games
- Six test programs; CI on GCC, Clang, GCC with sanitizers and MSVC, warnings as errors

### 🧮 [Math Expression Evaluator](https://github.com/IliaRakhlevski/Math-Expression-Evaluator)

A C++17 evaluator for infix arithmetic expressions, converting them to Reverse Polish Notation via Dijkstra's Shunting Yard algorithm and evaluating on a value stack.

Key features:

- Table-driven token validation and operator precedence/associativity, instead of ad-hoc conditionals
- Token represented as std::variant, with enum class used throughout
- Every failure reported as a specific error code rather than a silently wrong number
- Exact-zero divisor check, so results like 1 / 1e-20 remain valid
- Verified against a reference implementation on hundreds of random expressions, with zero discrepancies
- Continuous integration on GCC, Clang, and MSVC

### 🚗 [Parking System](https://github.com/IliaRakhlevski/Parking-System)

Distributed parking management system in C and C++ integrating STM32 firmware, a BeagleBone Green client on Embedded Linux, and multi-process server applications on Linux.

Key features:

- Multi-process Linux architecture with POSIX threads and synchronization
- TCP/IP communication between embedded clients and an event-driven server
- System V shared memory, shared queues, unnamed pipes, and POSIX signals
- SQLite-based parking-session and tariff management
- STM32-to-BeagleBone integration over I²C, with the client started automatically by systemd

### 🛣️ [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector)

Real-time road impact candidate detection and GNSS localization system built on STM32F756ZG and FreeRTOS.

Key features:

- Interrupt-driven ICM-20948 IMU acquisition at approximately 102 samples per second
- Quectel LC86G-LA GNSS positioning with PPS-based hardware timestamp capture
- Common TIM2 timebase for synchronizing IMU measurements with GNSS time
- Acceleration-baseline algorithm associating impact candidates with UTC timestamps and coordinates
- Real-hardware validation with documented field-test output, photographs, and video

### 🔧 [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester)

Automated hardware validation system for STM32F756ZG peripherals using FreeRTOS and a Linux UDP test host.

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
- Dynamic management of emergency vehicle availability, interrupted-event retries, and fault recovery, validated through a continuous 10-hour stress test
