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

### 🚢 [Sea Battle](https://github.com/IliaRakhlevski/Sea-Battle)

Battleship in C++17 with the classic 10-ship rules (ships may not touch, a hit earns another shot), designed as a reusable game-rules library with a separate console front end.

Key features:

- Rules library with no I/O: board, fleet placement, shooting and game session are independent of the UI
- Pluggable placement and targeting strategies (Strategy), game events for any front end (Observer), dependency injection via `std::unique_ptr`
- Modern C++17: `std::optional`, `std::variant`, RAII, value types, `[[nodiscard]]`
- Computer strategies compared by measurement on simulated games
- Six test programs; CI on GCC, Clang, GCC with sanitizers and MSVC, warnings as errors

### 🚨 [City Emergency Dispatch](https://github.com/IliaRakhlevski/City-Emergency-Dispatch)

Real-time emergency dispatch simulation in C on FreeRTOS POSIX (Linux): a server generates city events and a client processes them with priority-based vehicle tasks.

Key features:

- Independent FreeRTOS tasks per vehicle, with department-specific priority queues
- Synchronization with queues, mutexes and event groups
- Fault Manager with automatic retry of interrupted events, and Shift Manager for dynamic vehicle availability
- UDP client-server communication with acknowledgements and completion reports
- SQLite event persistence and runtime statistics under stress testing

### 🚗 [Parking System](https://github.com/IliaRakhlevski/Parking-System)

Distributed parking management system in C and C++ integrating STM32 firmware, a BeagleBone Green client on Embedded Linux, and multi-process server applications on Linux.

Key features:

- Multi-process Linux architecture with POSIX threads and synchronization
- TCP/IP communication between embedded clients and an event-driven server
- System V shared memory, shared queues, unnamed pipes, and POSIX signals
- SQLite-based parking-session and tariff management
- STM32-to-BeagleBone integration over I²C, with the client started automatically by systemd

### 🔧 [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester)

Automated hardware validation system written in C for STM32F756ZG peripherals, using FreeRTOS and a Linux UDP test host.

Key features:

- Concurrent validation of UART, SPI, I²C, ADC, DAC, and timer peripherals
- Interrupt- and DMA-based test modes
- Automated PASS/FAIL evaluation with random payload generation and CRC verification
- UDP communication between the STM32 firmware and Linux server
- Runtime statistics and persistent test results stored in SQLite

### 🛣️ [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector)

Real-time road impact candidate detection and GNSS localization system written in C, built on STM32F756ZG and FreeRTOS.

Key features:

- Interrupt-driven ICM-20948 IMU acquisition at approximately 102 samples per second
- Quectel LC86G-LA GNSS positioning with PPS-based hardware timestamp capture
- Common TIM2 timebase for synchronizing IMU measurements with GNSS time
- Acceleration-baseline algorithm associating impact candidates with UTC timestamps and coordinates
- Real-hardware validation with documented field-test output, photographs, and video

### 🧠 [Image Classification with ResNet18](https://github.com/IliaRakhlevski/Classification-of-One-Piece-characters-using-ResNet18)

Image classification of 18 character classes from a public Kaggle dataset in Python and PyTorch, using transfer learning on a pretrained ResNet18.

Key features:

- Transfer learning: pretrained layers frozen, new classification head, `layer3` and `layer4` fine-tuned
- Dataset split that keeps all variants of the same source image in one subset, to prevent leakage between training, validation and test sets
- Reproducibility checked across several random seeds
- 91.7% test accuracy, with a normalized confusion matrix and analysis of highly confident misclassifications

