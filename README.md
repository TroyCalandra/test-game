## C to WASM games
a compilation of games built with C and SDL compiled to WebAssembly through [Emscripten](https://emscripten.org/).

## Pre reqs
https://github.com/emscripten-core/emsdk
CMake
Git

## Snake Compile to WASM
Compile
```
snake/src/ $ emcc -02 \
 -o opt.html *.c \
 -Wall -g -lm \
 -s USE_SDL=2
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