# Testing project for Rust Wii

## Requirements
Install devkitPro with development dependencies:
* Download from `https://devkitpro.org/wiki/devkitPro_pacman`
* Execute `sudo gdebi devkitpro-pacman.amd64.deb` to install
* Install Wii development tools:
  * `sudo dkp-pacman -S wii-dev` for debian based
  * `sudo pacman -S wii-dev` for distros with pacman

## Build
`cargo +nightly build -Z build-std=core,alloc --target powerpc-unknown-eabi.json` to compile.

Output will be an extensionless file on `testing-project/target/powerpc-unknown-eabi/debug/` with file name as project name (same on bin). To run it on dolphin emulator, you must add its extension that is `.elf`
