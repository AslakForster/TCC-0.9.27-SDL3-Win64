README
Please read the included license files before you begin.

TCC 0.9.27 Win64 with SDL3 and SDL3_ttf preconfigured
This package contains a pre-built Tiny C Compiler (TCC) 0.9.27 for Windows 64-bit, together with:

- A complete set of WinAPI headers for TCC
- SDL3 a cross-platform software development library.
- SDL3_ttf helps users render text in SDL3 apps.
- Example programs

Build & run on Windows
Recommended:
  Run compile_main.c.bat to compile main.c.

Manual (Command Prompt):
1) Open Command Prompt (cmd.exe)
2) Navigate to the folder containing tcc.exe

Compile:
  tcc.exe -o main.exe main.c -lgdi32 -lSDL3_ttf -lSDL3 -lopengl32 -mwindows

Run:
  main.exe

Notes:
- -mwindows builds a GUI subsystem executable (no console window). When compiling CMD apps, omit -mwindows.
- If the program fails to start, make sure SDL3.dll and SDL3_ttf.dll are in the same folder as the executable.

Build & run on Linux using Wine
Compile:
  WINEDEBUG=-all wine tcc.exe -o main.exe main.c -lgdi32 -lSDL3_ttf -lSDL3 -lopengl32 -mwindows

Run:
  WINEDEBUG=-all wine main.exe

Note:
- To see Wine diagnostics, remove WINEDEBUG=-all.
