## C to WASM games
a compilation of games built with C and SDL compiled to WebAssembly through [Emscripten](https://emscripten.org/).

## Pre reqs
https://github.com/emscripten-core/emsdk
CMake
Git

## Snake Compile to WASM
Compile to single file
```
snake/src/ $ emcc -o single.html *.c -s WASM=1 -s SINGLE_FILE=1 -s USE_SDL=2
```
or

Compile to multiple files
```
snake/src/ $ emcc -o output.html *.c -s USE_SDL=2
```
Run
```
npx http-server .
```

## Snake Compile to Native
Compile
```
snake/src/ $ clang -o program main.c `pkg-config --cflags --libs sdl2` ./snake.c ./apple.c
```
Run
```
./program
```
## Tutorial
https://dev.to/kibebr/i-made-a-game-in-c-run-in-a-web-browser-and-so-can-you-4deb