# cpp-toy-chat


## Installation

### Install Ubuntu

`install conan`

```terminal
pip install conan
```

`install cmake`

```terminal
sudo apt install cmake
```

### Install Windows

## Conan Configuration

```terminal
conan profile detect --force
conan install . --output-folder=build --build=missing

cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
cmake --build .
```
