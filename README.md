# Steam Engine: OpenGL Simulation

A 3D animated steam engine (piston, crank and flywheel) built in C with OpenGL/GLUT. Made as a computer graphics mini-project, based on the classic OpenGL steam engine example.

## Features
- Animated piston, crankshaft and flywheel
- Rotate the view, change animation speed
- Toggle shading, textures, transparency and two light sources

## Tech stack
C · OpenGL · GLUT · Code::Blocks

## Build
Needs a GLUT library (for example freeglut).
```
gcc main.cpp -o steam_engine -lfreeglut -lopengl32 -lglu32
```
Or open `steam_engin.cbp` in Code::Blocks and build.
