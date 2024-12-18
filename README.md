# Prefix

:triangular_flag_on_post: **Windows only!** As on GNU/Linux usually all those
thirdparty libraries are available in some distribution repository.

A collection of third party libraries and scripts to build a third party
prefix directory for a Windows build of our games.

## Version

- SDL: 2.30.10
- SDL_net: 2.2.0
- SDL_image: 2.8.3
- SDL_mixer: 2.8.0
- GLEW 2.2.0
- GLM 1.0.1

## Checkout

```bash
git clone https://github.com/leftoverspecs/prefix.git
cd prefix
git submodule update --init
cd protobuf
git submodule update --init third_party\abseil-cpp
```

## Build

```bash
# Debug build
cmake --preset debug
cmake --build --preset debug
cmake --install build\debug --config Debug --prefix build\debug\dist

# Release build
cmake --preset release
cmake --build --preset release
cmake --install build\release --config Release --prefix build\release\dist
```

## Usage

```bash
mkdir build && cd build
cmake -DCMAKE_PREFIX_PATH=<path-to-repo>/build/<config>/dist ..
```
