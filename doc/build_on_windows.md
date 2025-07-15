# Build on Windows

## Environment
1. Download and install [Msys2](https://www.msys2.org/).
2. Open `ucrt64.exe` and run `pacman -Syu` to update packages.
3. Run `pacman -S make mingw-w64-ucrt-x86_64-gcc mingw-w64-ucrt-x86_64-dlfcn` to install required packages.

## Build
1. Open `ucrt64.exe` and run `cd /path/to/project` to change directory.
2. Run `make -j$(getconf _NPROCESSORS_ONLN) CONFIG_WERROR=y` to build.
3. Get the library file `libquickjs.a` under `/path/to/project`.
`