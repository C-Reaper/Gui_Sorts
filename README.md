# Project README

## Overview
This project is a simple sorting visualization application developed in C. It allows users to visually observe the process of different sorting algorithms such as Bubble Sort, Insertion Sort, Selection Sort, Merge Sort, and Quick Sort.

## Features
- Visualization of various sorting algorithms.
- Real-time rendering of sorting steps.
- Interactive control over the size of the data set and selection of sorting algorithm.

## Project Structure
The project structure is organized as follows:
```
<Project>/
├── src/                # Source code directory
│   ├── Main.c          # Entry point file
│   └── *.h             # Header files used by Main.c
├── Makefile.linux      # Linux build configuration
├── Makefile.windows    # Windows build configuration
├── Makefile.wine       # Wine build configuration for cross-compiling to Windows
├── Makefile.web        # Emscripten build configuration for WebAssembly
└── README.md           # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed:
  - For Linux: X11, PNG, JPEG
  - For Windows: WINAPI
  - For WebAssembly: Emscripten

## Build & Run
### Build on Linux
To build the project on a Linux system, follow these steps:
```sh
cd <Project>
make -f Makefile.linux all
```
This will compile the source code and generate an executable named `Main` in the `build` directory.

### Build on Windows
For Windows, use the following commands:
```sh
cd <Project>
make -f Makefile.windows all
```
This will create an executable named `Main.exe` in the `build` directory using MinGW.

### Build for WebAssembly
To build the project for web deployment, use Emscripten:
```sh
cd <Project>
make -f Makefile.web all
```
This will compile the source code and generate HTML, JavaScript, and WebAssembly files in the `build` directory. You can serve the `index.html` file using a web server to view the application.

### Execute
After building, you can run the executable as follows:
```sh
# On Linux
make -f Makefile.linux exe

# On Windows
make -f Makefile.windows exe
```
For WebAssembly, open the `index.html` file in a web browser to interact with the application.

### Clean Build
To clean the build artifacts and start fresh, use:
```sh
make -f Makefile.linux clean
```
This will remove all files generated during the build process.