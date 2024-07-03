---

# Operating System Project - Phase 1

This project is part of an academic course on operating systems, where we simulate an operating system's basic functionalities such as job scheduling, instruction execution, and data handling. The project is implemented in C++ and includes key concepts such as reading from input files, processing instructions, and writing to output files.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Contributing](#contributing)
- [License](#license)

## Introduction
This project simulates a simple operating system that can read job instructions, execute them, and manage data input and output. It includes functionalities for initializing memory, handling different instructions, managing execution flow, and logging the results.

## Features
- Job scheduling
- Instruction execution (`GD`, `PD`, `H`, `LR`, `SR`, `CR`, `BR`)
- Memory management
- Input and output handling

## Tech Stack
- **Programming Language:** C++
- **Libraries:** Standard C++ Libraries (iostream, fstream, string)

## Prerequisites
- C++ compiler (g++ recommended)

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/OmkarLolage21/OS_Phase1.git
   cd OS_Phase1
   ```

2. Ensure you have a C++ compiler installed. For g++:
   ```bash
   sudo apt-get install g++
   ```

## Usage
1. Compile the program:
   ```bash
   g++ OS_phase1.cpp -o os_phase1
   ```

2. Create an input file `inputPhase1.txt` with job instructions in the project directory.

3. Run the executable:
   ```bash
   ./os_phase1
   ```

4. Output will be generated in the `output.txt` file.

## Code Explanation

### Initialization

The `INIT` function initializes the memory, instruction register, general-purpose register, instruction counter, service interrupt, and toggle register.

### Instructions

- **GD (Get Data):** Reads data from the input file and stores it in memory.
- **PD (Put Data):** Writes data from memory to the output file.
- **H (Halt):** Ends the job and writes two new lines to the output file.
- **LR (Load Register):** Loads data from a specified memory location to the general-purpose register `R`.
- **SR (Store Register):** Stores data from the general-purpose register `R` to a specified memory location.
- **CR (Compare):** Compares data at a specified memory location with the contents of the general-purpose register `R`.
- **BR (Branch):** Branches the execution flow to a specified memory location if the comparison condition is met.

### Execution Flow

The `LOAD` function reads jobs from the input file and stores instructions in memory. The `STARTEXECUTION` function starts the execution of the user program, and `EXECUTEUSERPROGRAM` manages the execution of instructions.

### Master Mode

The `MOS` function handles service interrupts for different operations (input, output, and halt).

### Slave Mode

The `EXECUTEUSERPROGRAM` function runs the user program by fetching and executing instructions stored in memory.

## Contributing
Contributions are welcome! Please follow these steps to contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature-name`).
5. Open a Pull Request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
