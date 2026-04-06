# Retro Car Racing 2.0

## Project Description
Retro Car Racing 2.0 is a 2D local multiplayer top-down racing game developed using C++ and the OpenGL (GLUT) graphical API. Players compete head-to-head on a dynamically scrolling track, dodging moving traffic and managing essential resources to outlast their opponent.

## Features
- **Local Multiplayer:** Enjoy competitive dual-player functionality on a single keyboard.
- **Dynamic Scenery:** Experience a rich track environment including roads, buildings, pine trees, lakes, and lampposts.
- **Resource Management:** Both players begin with 3 lives and limited fuel. Replenishments and abilities can be earned while racing.
- **Obstacles & Collision Detection:** Moving traffic including civilian cars, trucks, and police cruisers make the track challenging. The game features robust collision detection resulting in life reduction or round completion.
- **Interactive UI:** Smooth user interface transitions including a detailed Starting Screen, Instruction Manual, and a Game Over results display with a winner's trophy.
- **Audio Effects:** Menu navigation logic, engine roars, and collision sounds provide an immersive arcade experience.

## Gameplay Controls

### Player 1 (Blue Car)
- **Steer Left:** `A`
- **Steer Right:** `D`

### Player 2 (Red Car)
- **Steer Left:** `Left Arrow`
- **Steer Right:** `Right Arrow`

### General Navigational Controls
- **Navigate Menus:** `Up Arrow` / `Down Arrow`
- **Select Option:** `Enter`
- **Return to Menu:** `Esc`
- **Toggle Fullscreen:** `Shift + F`
- **Quick Exit Game:** `X` 

## Setup and Installation

### Prerequisites
- C++ Compiler (e.g., MinGW, GCC).
- OpenGL Library (GLUT or FreeGLUT).
- Code::Blocks IDE (Recommended, as native project files are included).
- Windows Operating System for comprehensive sound library support using Windows system libraries.

### Build Instructions
1. Clone or download the source code to your local machine.
2. Open the `car_racing.cbp` project workspace file in the Code::Blocks IDE.
3. Ensure GLUT headers and libraries are properly linked in your IDE compiler settings:
   - Link the core libraries: `opengl32`, `glu32`, and `glut32` (or `freeglut`).
   - Link `winmm` within the linker settings for audio rendering support.
4. Build and run the project from the IDE to launch the application.

## Core File Structure
- `main.cpp`: The entry point containing the game loop, initialization, and main display functions.
- `carKeyboard.h`: Centralized logic for vehicle handling, keyboard polling, and boundaries.
- `StartingPage.h` / `instructions.h` / `result.h`: Pre-game and end-game visual logic and text rendering routines.
- `vehicle.h` / `animation.h`: Core graphics instructions for drawing cars and rendering continuous movement.
- `obstacle.h` / `collision.h`: Procedural generation of traffic elements and state checkers for crashes.
- `scoreBoard.h`: Dashboard HUD overlay providing live metrics on distance, remaining fuel, and standard lives.
- `sound.h`: Wrapper logic for asynchronous Windows API audio delivery.
- Various environmental headers (`road.h`, `building.h`, `tree.h`, `lake.h`): Structural drawing subroutines representing stage backdrops.

## Technologies Used
- **C++:** Core business logic and control structures.
- **OpenGL/GLUT:** Native 2D graphics rendering, geometrical drawing, matrix calculations, and hardware inputs.
- **Windows.h:** Sound playback and execution delays.
