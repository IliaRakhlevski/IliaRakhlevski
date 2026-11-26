# Hi, I'm Ilia 👋

C/C++ Software Engineer with a strong track record in large-scale production desktop applications. Experienced in complex data processing, performance optimization, and debugging in long-lived codebases. Complemented by a multidisciplinary hardware/software background in embedded firmware for security and industrial systems. Featured below: recent projects in modern C++ (C++17), Linux systems programming and STM32/FreeRTOS firmware, along with machine learning projects in Python (signal processing and computer vision).

## Projects by Area

⭐ — featured below with details.

**Embedded, Real-Time & Linux**
- [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector) ⭐ — **C** · FreeRTOS, IMU + GNSS, PPS timing on STM32
- [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester) ⭐ — **C** · FreeRTOS firmware testing UART, SPI, I²C, ADC with a Linux UDP host
- [Parking System](https://github.com/IliaRakhlevski/Parking-System) ⭐ — **C, C++11** · distributed system: STM32, BeagleBone (Embedded Linux), multi-process Linux server
- [City Emergency Dispatch](https://github.com/IliaRakhlevski/City-Emergency-Dispatch) ⭐ — **C** · FreeRTOS multitasking on Linux, UDP, priority queues
- [Step and Servo Motors Control](https://github.com/IliaRakhlevski/Step-Servo-Motors-Control) — **C** · bare-metal ARM9, register-level PWM, GPIO, interrupts, ADC; no HAL

**C/C++ Software Design**
- [Sea Battle](https://github.com/IliaRakhlevski/Sea-Battle) ⭐ — **C++17** · game-rules library, Strategy and Observer, measured computer strategies
- [Vending Machine](https://github.com/IliaRakhlevski/Vending-Machine) — **C++17** · State-pattern FSM with tests for every transition
- [Math Expression Evaluator](https://github.com/IliaRakhlevski/Math-Expression-Evaluator) — **C++17** · Shunting Yard to RPN, stack evaluation
- [Custom Memory Manager in C](https://github.com/IliaRakhlevski/Custom-Memory-Manager-in-C) — **C11** · fixed-pool allocator without malloc, heap-corruption checks

**Computer Vision & Deep Learning**
- [Detection of Violence Against Children in Videos](https://github.com/IliaRakhlevski/Detection-of-violence-against-children-in-videos) ⭐ — **Python** · M.Sc. final project, CNN + LSTM, own dataset
- [Digits Recognition](https://github.com/IliaRakhlevski/Digits-Recognition) — **C++** · HOG and a neural network written from scratch
- [License Plates Recognition](https://github.com/IliaRakhlevski/License-Plates-Recognition) — **Python** · Faster R-CNN in PyTorch, self-annotated dataset
- [Traffic Signs Detection](https://github.com/IliaRakhlevski/Traffic-Signs-Detection) — **Python** · Mask R-CNN detection and recognition
- [One Piece Characters Classification](https://github.com/IliaRakhlevski/Classification-of-One-Piece-characters-using-ResNet18) — **Python** · transfer learning with ResNet18 in PyTorch

**Machine Learning, Audio & Simulation**
- [Tool Sound Classification](https://github.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods) ⭐ — **Python** · audio classification, peak envelopes and a 2D CNN
- [Speed Dating Experiment](https://github.com/IliaRakhlevski/Speed-Dating-Experiment) — **Python** · data analysis, five scikit-learn classifiers
- [Autonomous Road Merging Simulation](https://github.com/IliaRakhlevski/Simulation-of-Autonomous-Road-Merging) — **Python** · Pygame, FSM vehicle control, crashes cut from 45% to 6%

## Technical Focus

- **Languages:** Modern C++ (C++17), C, Python
- **Python:** NumPy, SciPy, Pandas, PyTorch, TensorFlow/Keras, OpenCV, scikit-learn, Pygame
- **Design Patterns:** State, Strategy, Observer, Dependency Injection, Composite, Factory Method, Command
- **AI-Assisted Development:** agentic and chat-based AI coding tools for implementation, architecture/design exploration, debugging and code review, with engineering validation of generated solutions
- **Testing & CI:** unit testing, reference-implementation verification, GitHub Actions on GCC/Clang/MSVC, sanitizers, warnings as errors, cross-compilation for ARM Cortex-M and Embedded Linux, end-to-end smoke tests
- **Concurrency & IPC:** POSIX threads, processes, mutexes, semaphores, condition variables, shared memory, pipes, signals
- **Networking & Storage:** TCP/IP, UDP, BSD sockets, SQLite
- **Linux Systems Programming:** POSIX APIs, multi-process applications, systemd
- **Embedded & Real-Time:** ARM Cortex-M (STM32), FreeRTOS, Embedded Linux, bare-metal firmware, HAL/CMSIS, LwIP, interrupt- and DMA-driven design; UART, SPI, I²C, ADC, DAC, GPIO, PWM
- **Machine Learning & Deep Learning:** CNNs, transfer learning (ResNet), object detection (Faster R-CNN), video classification (CNN + LSTM); dataset creation and annotation, data augmentation, leakage-aware data splits, error analysis
- **Signal, Image & Video Processing:** audio preprocessing (resampling, normalization, peak envelopes, sliding windows); image preprocessing with OpenCV (resizing with padding, normalization); video processing (frame extraction, fixed-length clips, sliding-window analysis of long videos)
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

### Linux Systems & Concurrency

#### 🚗 [Parking System](https://github.com/IliaRakhlevski/Parking-System)

Distributed parking management system in C and C++11 integrating STM32 firmware, a BeagleBone Green client on Embedded Linux, and multi-process server applications on Linux.

<a href="https://github.com/IliaRakhlevski/Parking-System"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Parking-System/main/Docs/Images/parking-system-overview.png" alt="Parking System overview" width="800"></a>

Key features:

- Multi-process Linux architecture with POSIX threads and synchronization
- TCP/IP communication between embedded clients and an event-driven server
- System V shared memory, shared queues, unnamed pipes, and POSIX signals
- SQLite-based parking-session and tariff management
- STM32-to-BeagleBone integration over I²C, with the client started automatically by systemd
- CI for all three platforms: Linux build and library smoke tests (also under ASan and UBSan), BeagleBone ARM cross-build, STM32 firmware build

#### 🚨 [City Emergency Dispatch](https://github.com/IliaRakhlevski/City-Emergency-Dispatch)

Emergency dispatch simulation in C on FreeRTOS (POSIX port on Linux): a server generates city events and a client dispatches them through priority-based event queues to vehicle tasks.

<a href="https://github.com/IliaRakhlevski/City-Emergency-Dispatch"><img src="https://raw.githubusercontent.com/IliaRakhlevski/City-Emergency-Dispatch/main/Docs/images/overview.png" alt="City Emergency Dispatch overview" width="800"></a>

Key features:

- Independent FreeRTOS tasks per vehicle, with department-specific priority queues
- Synchronization with queues, mutexes and event groups
- Fault Manager with automatic retry of interrupted events, and Shift Manager for dynamic vehicle availability
- UDP client-server communication with acknowledgements and completion reports
- SQLite event persistence and runtime statistics under stress testing
- CI: build and an end-to-end smoke test that runs the client and the server together over UDP and checks the event statistics

### Embedded Real-Time Firmware (STM32 + FreeRTOS)

#### 🔧 [STM32 Peripheral Tester](https://github.com/IliaRakhlevski/STM32-Peripheral-Tester)

Automated hardware validation system written in C for STM32F756ZG peripherals, using FreeRTOS and a Linux UDP test host.

<a href="https://github.com/IliaRakhlevski/STM32-Peripheral-Tester"><img src="https://raw.githubusercontent.com/IliaRakhlevski/STM32-Peripheral-Tester/main/docs/images/overview.png" alt="STM32 Peripheral Tester overview" width="800"></a>

Key features:

- Concurrent validation of UART, SPI, I²C, ADC (via DAC loopback), and timer peripherals
- Interrupt- and DMA-based test modes
- Automated PASS/FAIL evaluation with random payload generation and CRC verification
- UDP communication between the STM32 firmware and Linux server
- Runtime statistics and persistent test results stored in SQLite
- CI: firmware build (FreeRTOS + LwIP) with arm-none-eabi-gcc and Linux server build

#### 🛣️ [STM32 Road Impact Detector](https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector)

Real-time road impact candidate detection and GNSS localization system written in C, built on STM32F756ZG and FreeRTOS.

<a href="https://github.com/IliaRakhlevski/STM32-Road-Impact-Detector"><img src="https://raw.githubusercontent.com/IliaRakhlevski/STM32-Road-Impact-Detector/main/Docs/Images/overview.png" alt="STM32 Road Impact Detector overview" width="800"></a>

Key features:

- Interrupt-driven ICM-20948 IMU acquisition at approximately 102 samples per second
- Quectel LC86G-LA GNSS positioning with PPS-based hardware timestamp capture
- Common TIM2 timebase for synchronizing IMU measurements with GNSS time
- Acceleration-baseline algorithm associating impact candidates with UTC timestamps and coordinates
- Real-hardware validation with documented field-test output, photographs, and video
- CI: firmware build with arm-none-eabi-gcc

### Machine Learning

#### 🔊 [Tool Sound Classification](https://github.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods)

Classification of tool sounds (hammer, jackhammer, drill) in Python, designed for real-time classification on a standard PC (CPU only): time-domain signal processing with a 2D CNN in Keras/TensorFlow.

<a href="https://github.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Classification-of-tools-sounds-using-machine-learning-methods/main/images/overview.png" alt="Tool Sound Classification overview" width="800"></a>

Key features:

- Signal preprocessing with NumPy/SciPy: resampling to 8 kHz, normalization to [-1, 1], fixed 4000-sample frames with zero padding
- Two-level peak envelope extraction in the time domain as a simple, interpretable signal representation
- Sliding-window classification with 50% overlap, a weak-signal threshold and per-file majority voting
- Drill and jackhammer recognized reliably; error analysis of hammer/jackhammer confusion and dataset limitations documented in the README

#### 📹 [Detection of Violence Against Children in Videos](https://github.com/IliaRakhlevski/Detection-of-violence-against-children-in-videos)

M.Sc. final project: detection of physical violence of adults against children in surveillance videos with a CNN + LSTM model in Python and Keras/TensorFlow, trained on an own staged dataset.

<a href="https://github.com/IliaRakhlevski/Detection-of-violence-against-children-in-videos"><img src="https://raw.githubusercontent.com/IliaRakhlevski/Detection-of-violence-against-children-in-videos/main/images/overview.png" alt="Detection of Violence Against Children in Videos overview" width="800"></a>

Key features:

- Own dataset of about 8,000 20-frame clips recorded with reborn dolls instead of children; both classes are recorded in the same scene, so the model learns from the movement only
- ResNet152V2 (ImageNet-pretrained, frozen) extracts the features of each frame; a bidirectional LSTM classifies the movement over 20 frames
- Sliding-window processing of long surveillance videos, with merging of the detected violent fragments
- Tested on 120 videos (45,850 frames) of four types: staged, real with violence, real without violence, empty rooms
- 86% of violent frames detected and 91% of non-violent frames classified correctly; real test videos are kept out of the repository for privacy

## Contact

- Email: [rakhlevski@gmail.com](mailto:rakhlevski@gmail.com)
- LinkedIn: [linkedin.com/in/ilia-rakhlevski](https://www.linkedin.com/in/ilia-rakhlevski/)

