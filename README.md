# Hi, I'm Ilia 👋

C/C++ Software Engineer with a strong track record in large-scale production desktop applications. Experienced in complex data processing, performance optimization, and debugging in long-lived codebases. Complemented by a multidisciplinary hardware/software background in embedded firmware for security and industrial systems. Recent projects in modern C++ (C++17), Linux systems programming, STM32/FreeRTOS firmware, and Python/PyTorch are featured below.

## Technical Focus

- **Languages:** Modern C++ (C++17), C, Python
- **Modern C++:** C++17 idioms (variant, optional, RAII), smart pointers, templates
- **Python:** NumPy, SciPy, Pandas, PyTorch, TensorFlow/Keras, OpenCV, scikit-learn, Pygame
- **Design Patterns:** State, Strategy, Observer, Dependency Injection, Composite, Factory Method, Command
- **AI-Assisted Development:** agentic and chat-based AI coding tools for implementation, architecture/design exploration, debugging and code review, with engineering validation of generated solutions
- **Testing & CI:** unit testing, reference-implementation verification, GitHub Actions on GCC/Clang/MSVC, sanitizers, warnings as errors
- **Concurrency & IPC:** POSIX threads, processes, mutexes, semaphores, condition variables, shared memory, pipes, signals
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, SQLite
- **Linux Systems Programming:** POSIX APIs, multi-process applications, systemd
- **Embedded & Real-Time:** ARM Cortex-M (STM32), FreeRTOS, Embedded Linux, bare-metal firmware, HAL/CMSIS, LwIP, interrupt- and DMA-driven design; UART, SPI, I²C, ADC, DAC, GPIO, PWM
- **Development Tools:** Git, GNU Make, CMake, SVN, VS Code, Visual Studio

## Featured Projects

### Modern C++

#### 🚢 [Sea Battle](https://github.com/IliaRakhlevski/Sea-Battle)

Battleship in C++17 with the classic 10-ship rules (ships may not touch, a hit earns another shot), designed as a reusable game-rules library with a separate console front end.

<a href="https://github.com/IliaRakhlevski/Sea-Battle"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Sea-Battle/master/docs/images/overview.png" alt="Sea Battle overview" width="800"></a>

Key features:

- Rules library with no I/O: board, fleet placement, shooting and game session are independent of the UI
- Pluggable placement and targeting strategies (Strategy), game events for any front end (Observer), dependency injection via `std::unique_ptr`
- Modern C++17: `std::optional`, `std::variant`, RAII, value types, `[[nodiscard]]`
- Computer strategies compared by measurement on simulated games
- Six test programs; CI on GCC, Clang, GCC with sanitizers and MSVC, warnings as errors

### Linux Systems & Real-Time

#### 🚗 [Parking System](https://github.com/IliaRakhlevski/Parking-System)

Distributed parking management system in C and C++ integrating STM32 firmware, a BeagleBone Green client on Embedded Linux, and multi-process server applications on Linux.

<a href="https://github.com/IliaRakhlevski/Parking-System"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Parking-System/main/Docs/Images/parking-system-overview.png" alt="Parking System overview" width="800"></a>

Key features:

- Multi-process Linux architecture with POSIX threads and synchronization
- TCP/IP communication between embedded clients and an event-driven server
- System V shared memory, shared queues, unnamed pipes, and POSIX signals
- SQLite-based parking-session and tariff management
- STM32-to-BeagleBone integration over I²C, with the client started automatically by systemd

#### 🚨 [City Emergency Dispatch](https://github.com/IliaRakhlevski/City-Emergency-Dispatch)

Real-time emergency dispatch simulation in C on FreeRTOS POSIX (Linux): a server generates city events and a client processes them with priority-based vehicle tasks.

<a href="https://github.com/IliaRakhlevski/City-Emergency-Dispatch"><img src="https://raw.githubusercontent.com/IliaRakhlevski/City-Emergency-Dispatch/main/Docs/images/overview.png" alt="City Emergency Dispatch overview" width="800"></a>

Key features:

- Independent FreeRTOS tasks per vehicle, with department-specific priority queues
- Synchronization with queues, mutexes and event groups
- Fault Manager with automatic retry of interrupted events, and Shift Manager for dynamic vehicle availability
- UDP client-server communication with acknowledgements and completion reports
- SQLite event persistence and runtime statistics under stress testing

### Embedded Firmware (STM32)

#### 🔧 [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester)

Automated hardware validation system written in C for STM32F756ZG peripherals, using FreeRTOS and a Linux UDP test host.

<a href="https://github.com/IliaRakhlevski/STM32-Peripheral-Tester"><img src="https://raw.githubusercontent.com/IliaRakhlevski/STM32-Peripheral-Tester/main/docs/images/overview.png" alt="STM32 Peripheral Tester overview" width="800"></a>

Key features:

- Concurrent validation of UART, SPI, I²C, ADC (via DAC loopback), and timer peripherals
- Interrupt- and DMA-based test modes
- Automated PASS/FAIL evaluation with random payload generation and CRC verification
- UDP communication between the STM32 firmware and Linux server
- Runtime statistics and persistent test results stored in SQLite

#### 🛣️ [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector)

Real-time road impact candidate detection and GNSS localization system written in C, built on STM32F756ZG and FreeRTOS.

<a href="https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector"><img src="https://raw.githubusercontent.com/IliaRakhlevski/STM32-Road-Impact-Detector/main/Docs/Images/overview.png" alt="STM32 Road Impact Detector overview" width="800"></a>

Key features:

- Interrupt-driven ICM-20948 IMU acquisition at approximately 102 samples per second
- Quectel LC86G-LA GNSS positioning with PPS-based hardware timestamp capture
- Common TIM2 timebase for synchronizing IMU measurements with GNSS time
- Acceleration-baseline algorithm associating impact candidates with UTC timestamps and coordinates
- Real-hardware validation with documented field-test output, photographs, and video

### Machine Learning

#### 🔊 [Tool Sound Classification](https://github.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods)

Classification of tool sounds (hammer, jackhammer, drill) in Python, designed for real-time classification on a standard PC (CPU only): time-domain signal processing with a 2D CNN in Keras/TensorFlow.

<a href="https://github.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods/main/images/overview.png" alt="Tool Sound Classification overview" width="800"></a>

Key features:

- Signal preprocessing with NumPy/SciPy: resampling to 8 kHz, normalization to [-1, 1], fixed 4000-sample frames with zero padding
- Two-level peak envelope extraction in the time domain as a simple, interpretable signal representation
- Sliding-window classification with 50% overlap, a weak-signal threshold and per-file majority voting
- Drill and jackhammer recognized reliably; error analysis of hammer/jackhammer confusion and dataset limitations documented in the README

## Contact

- Email: [rakhlevski@gmail.com](mailto:rakhlevski@gmail.com)
- LinkedIn: [linkedin.com/in/ilia-rakhlevski](https://www.linkedin.com/in/ilia-rakhlevski/)

