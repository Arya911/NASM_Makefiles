# NASM Makefiles

This repository contains two Makefiles for assembling and linking assembly code written for the Netwide Assembler (NASM). These Makefiles are tailored for 32-bit and 64-bit architectures.

## Makefiles Overview

### Makefile 1: 32-bit
This Makefile is used to assemble and link assembly code for 32-bit architectures.

- **Assembler:** NASM
- **Linker:** GNU LD
- **File format:** ELF

#### Key Variables
- `ASM`: Path to NASM (default: `nasm`)
- `ASM_FLAGS`: `-f elf` (32-bit format)
- `LD_FLAGS`: `-m elf_i386` (32-bit linker flag)

### Makefile 2: 64-bit
This Makefile is used to assemble and link assembly code for 64-bit architectures.

- **Assembler:** NASM
- **Linker:** GNU LD
- **File format:** ELF64

#### Key Variables
- `ASM`: Path to NASM (default: `nasm`)
- `ASM_FLAGS`: `-f elf64` (64-bit format)
- `LD_FLAGS`: `-m elf_x86_64` (64-bit linker flag)

## Usage

### Preparing Assembly Files
Ensure your assembly files (`.asm`) are in the same directory as the desired Makefile.

### Build All Files
To build all `.asm` files in the directory:
```bash
make
```
This will generate executables for each `.asm` file.

### Build a Specific File
To build a specific assembly file (e.g., `example.asm`):
```bash
make example
```
This will generate an executable named `example`.

### Clean Up
To remove all object files and executables:
```bash
make clean
```

## Switching Between 32-bit and 64-bit
- Use **Makefile 1** for 32-bit assembly code.
- Use **Makefile 2** for 64-bit assembly code.

Rename the appropriate Makefile to `Makefile` or specify it explicitly during the `make` command:
```bash
make -f Makefile32
make -f Makefile64
```

## Prerequisites

- **NASM**: Ensure NASM is installed on your system. Install via package managers:
  ```bash
  sudo apt install nasm  # Debian/Ubuntu
  brew install nasm      # macOS
  ```
- **GNU LD**: The GNU Linker (`ld`) must be available in your PATH.

## License
This project is open-source and available under the [MIT License](LICENSE).

## Contributions
Contributions are welcome! Feel free to open issues or submit pull requests.
