# PrettyWSL

A professional fork of Windows Subsystem for Linux (WSL) with enhanced features, custom kernel, and full rebranding.

## Components

| Component | Repository | Description |
|-----------|-----------|-------------|
| `wsl/` | [zsh4k/WSL](https://github.com/zsh4k/WSL) | Windows Subsystem for Linux (main source) |
| `kernel/` | [zsh4k/WSL2-Linux-Kernel](https://github.com/zsh4k/WSL2-Linux-Kernel) | Custom Linux kernel with PrettyWSL config |
| `wslg/` | [zsh4k/wslg](https://github.com/zsh4k/wslg) | WSLg - GUI app support (Wayland/X11) |
| `docs/` | [zsh4k/WSL-1](https://github.com/zsh4k/WSL-1) | Documentation fork |

## Features

- Custom kernel version: `-prettywsl-v1`
- Binary prefix: `pwsl` (e.g., `pwsl.exe`, `pwslservice.exe`)
- Enhanced kernel features: ZSWAP, SPI, ZRAM multi-compression (zstd+lz4+lzo)
- Full branding: PrettyWSL Project

## Build Requirements

- Windows 11 SDK 10.0.26100.0
- Visual Studio 2022 with C++ Clang Compiler for Windows
- CMake 3.25+

## Quick Start

```bash
# Clone with submodules
git clone --recursive https://github.com/zsh4k/PrettyWSL.git
cd PrettyWSL

# Build Windows components
cd wsl
cmake -B build -G "Visual Studio 17 2022" -A x64
cmake --build build
```
