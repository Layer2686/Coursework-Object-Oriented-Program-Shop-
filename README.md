Simple C++ project created in purpose to understand basic principles of OOP. Program simulates online shopp app.

# Build guide

This project uses CMake and requires a C++17-compatible compiler.

## Requirements

- CMake 3.30 or newer
- C++17 compiler:
  - GCC 8+
  - Clang 10+
  - MSVC 2019/2022
- Git (optional, if you clone the repository)

## 1. Clone the repository

```bash
git clone https://github.com/Layer2686/Coursework-Object-Oriented-Program-Shop-.git
cd Coursework-Object-Oriented-Program-Shop-
```

## 2. Build the project

### Linux

```bash
mkdir -p build
cd build
cmake ..
cmake --build .
```

Run the executable:

```bash
./KursovaCPP
```

For a Release build:

```bash
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build .
./KursovaCPP
```

### macOS

```bash
mkdir -p build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build .
```

Run the executable:

```bash
./KursovaCPP
```

If Xcode command line tools are not installed yet:

```bash
xcode-select --install
```

### Windows (Visual Studio)

From the project root:

```powershell
mkdir build
cd build
cmake .. -G "Visual Studio 17 2022"
cmake --build . --config Release
```

Run the executable:

```powershell
.\build\Release\KursovaCPP.exe
```

You can also open the generated solution file in the `build` folder with Visual Studio.

### Windows (MinGW / GCC)

```powershell
mkdir build
cd build
cmake .. -G "MinGW Makefiles"
cmake --build .
```

Run the executable:

```powershell
.\KursovaCPP.exe
```

If `cmake` does not recognize the compiler, verify that `g++` is installed:

```powershell
g++ --version
```

### Windows / Linux / macOS with Ninja

```bash
cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

## 3. Troubleshooting

- If CMake reports a version error, install CMake 3.30 or newer.
- If the compiler is not found, install the required toolchain:
  - Ubuntu/Debian: `sudo apt install build-essential cmake`
  - Fedora: `sudo dnf install gcc-c++ cmake`
  - macOS: `brew install cmake`
  - Windows: install Visual Studio 2022 with the C++ workload or MinGW
- If the project does not build, make sure you are in the repository root and that `CMakeLists.txt` is present.

## 4. Project output

The executable target is named:

```text
KursovaCPP
```

This project is configured in `CMakeLists.txt` with:

- C++17 standard
- single executable target `KursovaCPP`
- source files: `main.cpp`, `CUser.cpp`, `CProduct.cpp`, `Catalog.cpp`, `CAdmin.cpp`, `CBuyer.cpp`, and related headers
