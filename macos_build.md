
# Building for macOS

1. To fix "missing SDL.h":
```
brew install sdl2
```

Change Makefile SDL_INCLUDE_PATH:
```
ifeq ($(OS),Darwin)
SDL_INCLUDE_PATH:=/usr/local/Cellar/sdl2/2.26.0/include/SDL2
```


2. Download glew source code from https://github.com/nigels-com/glew. Run `make` in auto dir (change `python` in Makefile to `python3` if needed). Then run `make` in root.
3. Copy compiled `lib` folder into `glew/lib` in blastem repo
4. Run `./build_release`