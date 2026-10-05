# Hi, I'm Ilia 👋

C/C++ Software Engineer with a strong track record in large-scale production desktop and application-level software, complemented by a multidisciplinary hardware/software background in embedded and real-time systems.

My background includes enterprise CAD/EDA applications, real-time robot-control software, and commercial firmware for security and industrial systems. Recent hands-on projects — spanning modern C++, Linux systems, and embedded real-time development — reflect this range across both application-level and hardware-facing work.

## Technical Focus

- **Languages:** Modern C++ (C++17), C
- **Modern C++:** C++17 idioms (variant, optional, RAII), smart pointers, templates
- **Design Patterns:** State, Strategy, Observer, Dependency Injection, Composite, Factory Method, Command
- **AI-Assisted Development:** agentic and chat-based AI coding tools for implementation, architecture/design exploration, debugging and code review, with engineering validation of generated solutions
- **Testing & CI:** unit testing, reference-implementation verification, GitHub Actions on GCC/Clang/MSVC, sanitizers, warnings as errors
- **Concurrency & IPC:** POSIX threads, processes, mutexes, semaphores, condition variables, shared memory, pipes, signals
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, LwIP, Ethernet, SQLite
- **Real-Time & RTOS:** FreeRTOS, task scheduling, synchronization, inter-task communication
- **Embedded Firmware:** bare-metal ARM, STM32 HAL/CMSIS, direct memory-mapped register access, interrupt- and DMA-driven firmware
- **Embedded Linux:** Linux system programming, POSIX APIs, multi-process applications, systemd
- **Hardware Platforms:** STM32 NUCLEO-F756ZG (ARM Cortex-M7), BeagleBone Green (TI Sitara AM3358 / ARM Cortex-A8), FriendlyARM Mini2440 (Samsung S3C2440 / ARM9)
- **Sensors & Actuators:** Pimoroni ICM-20948 IMU, Quectel LC86G-LA GNSS receiver, SG90 servo motor, 28BYJ-48 stepper motor
- **Hardware Interfaces & Control:** UART, SPI, I²C, ADC, DAC, GPIO, hardware timers, PWM
- **Development Tools:** Git, GNU Make, CMake, STM32CubeIDE, STM32CubeMX, VS Code, Visual Studio

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

### ☕ [Vending Machine](https://github.com/IliaRakhlevski/Vending-Machine)

A coffee vending machine in C++17 — the classic object-oriented design interview task — built as a small library around a finite state machine, with a console application on top.

Key features:

- State pattern: one class per state, one virtual method per event, with a transition table as the specification
- Library with no direct I/O: all output goes through a UI object writing to any `std::ostream`, so tests can read the "screen"
- Coin escrow and change-making: exact refund of inserted coins, "Exact change only" when change cannot be paid
- Tests for every row of the transition table
- Continuous integration on GitHub Actions

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

