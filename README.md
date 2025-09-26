![5](https://github.com/user-attachments/assets/4b81ccc1-9803-4ad0-b703-e07fdec9429a)

# Binux

Binux is a minimal, POSIX-compliant operating system kernel written from scratch in C and Assembly. It aims to provide a simple and educational platform for understanding OS design, with a basic terminal interface and support for core POSIX syscalls.

## Features

- VT102-compatible terminal interface
- Basic POSIX syscalls (`read`, `write`, `open`, `close`, `execve`, etc.)
- Kernel trap and exception handling
- Bootloader for switching to protected mode
- Simple userland process initialization

## Requirements

- GCC (C compiler)
- Binutils (for linking/assembly)
- QEMU or VirtualBox (for running Binux)
- Make

## How to Compile

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Juoelenis/Binux.git
   cd Binux
   ```

2. **Build the kernel and boot image:**
   ```sh
   make
   ```
   This will compile the kernel and produce a bootable image (e.g., `binux.img`).

## How to Run Binux

### Using QEMU

```sh
qemu-system-i386 -drive file=binux.img,format=raw
```
Or, if your build produces a floppy/ISO image:
```sh
qemu-system-i386 -fda binux.img
```

### Using VirtualBox

1. Create a new VM (choose "Other" or "Linux (32-bit)").
2. Add a new virtual hard disk and attach `binux.img` as a virtual floppy or hard disk.
3. Start the VM.

## Notes

- Binux is not a Linux distribution or a userland application. It's a standalone kernel intended for learning, hacking, and experimentation.
- You may need to provide your own userland programs for full shell/coreutils functionality.
- For development, Ubuntu 16.04 or newer is recommended as a build environment.

## License

MIT
