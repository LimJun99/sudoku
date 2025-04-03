# sudoku
A cross-platform Sudoku game implemented in C++, easy to operate via the command line. It can be used to relax during development breaks. With only a few hundred lines of code, beginners can easily grasp it.
Contributions are welcome! Feel free to add features or fix bugs through pull requests.

## Thank you to all contributors!
<a href="https://github.com/mayerui/sudoku/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=mayerui/sudoku" />
</a>

## Features
1. Cross-Platform / Compiler Support : Linux/Windows/macOS [![Linux](https://github.com/mayerui/sudoku/actions/workflows/ci-linux.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-linux.yml) [![Windows](https://github.com/mayerui/sudoku/actions/workflows/ci-windows.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-windows.yml) [![macOS](https://github.com/mayerui/sudoku/actions/workflows/ci-macos.yml/badge.svg)](https://github.com/mayerui/sudoku/actions/workflows/ci-macos.yml)
2. Multilingual Support: English / 中文
3. No Third-Party Library Dependencies
4. Runs in the Console

## Dependencies
1. CMake 3.12 or higher
2. C++17

## Build Instructions
``` shell
cmake -B build -S .
cmake --build build
```

## Run Instructions
The '**sudoku**' executable generated by the build process will be located in the '**bin**' directory.
``` shell
./sudoku # Start the game directly

./sudoku -l filename # Load the game progress from a file

./sudoku -h # Display help information
```

## Controls:
- **0 #** Delete the number entered
- **u #** Undo the previous move
- **Enter #** Attempt to solve the puzzle
- **Esc #** Exit the game

### Normal Mode Controls:
- w # Move cursor up ↑
- a # Move cursor left ←
- s # Move cursor down ↓
- d # Move cursor right →

### VIM Mode Controls:
- **k #** Move cursor up ↑
- **h #** Move cursor left ←
- **j #** Move cursor down ↓
- **l #** Move cursor right →

## Project Structure
```bash
│--.gitignore  
│--build.bat        // One-click build script for Windows  
│--build.sh         // One-click build script for Linux/macOS  
│--CMakeLists.txt   // CMake project file  
│--README.md     
└--src              // Source code directory  
   │--block.cpp     // Sudoku block class, represents rows, columns, and subgrids  
   │--block.h  
   │--color.h       // Color class  
   │--command.cpp   // Command class, implements undo functionality  
   │--command.h     
   │--common.h      // Common header file  
   │--input.cpp     // Input class  
   │--input.h   
   │--main.cpp      // Main entry file  
   │--scene.cpp     // Game scene class  
   │--scene.h   
   │--test.cpp      // Test file  
   │--test.h  
   └--utility.inl   // Some utility global functions  
```
