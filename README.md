# Winbox: The ARM64 Windows Emulator
This package contains a minimal rootfs which contains a QEMU VM configured to run Windows 11. The Winbox script can automatically download Windows 11 ARM64 through UUP packages, compiles them into a setup ISO file, and lets you install it with only a few commands.

## Installation
`tar -xJf winbox-11.tar.xz`

## Usage
First, `./start.sh`.

`winbox download` - Download and compile Windows 11 ISO file

`winbox install` - Mount setup ISO and driver disk, and start VM through VNC

`winbox start` - Start Windows VM

`winbox lowmem start` - Start VM with 2GB of RAM instead of 4GB

`winbox kvm [lowmem] [start/setup]` - Enable KVM acceleration (only if kernel supports KVM)

## Connection
To connect to the VM, use any VNC viewer app and connect to `127.0.0.1:5900`.

## Compatibility
Any ARM64 Linux machine (including Android phones), or other architectures supporting QEMU ARM64 userspace emulation.
