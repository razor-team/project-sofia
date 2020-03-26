# Project S.O.F.I.A

[![Build Status](https://travis-ci.com/razor-team/project-sofia.svg?branch=master)](https://travis-ci.com/razor-team/project-sofia)

## Description

High Level OS for `x86-64/IA-64/ARM` architecture processors.

Commonly it's Kernel, just with stdout & stdin interfaces via terminal.

I wanna to make unix-like syscalls/commands system and as is open the `HTTP API` for more global extending the OS via many other remote modules wich will be able to work with `OS Kernel` throughout `NET` packages transport protocols.

## Documents

* [OS DEV](https://wiki.osdev.org/Expanded_Main_Page)
* [Writing Simple OS](https://www.cs.bham.ac.uk/~exr/lectures/opsys/10_11/lectures/os-dev.pdf)
* [Little Book about OS DEV](https://littleosbook.github.io/)
* [QEMU](https://www.qemu.org/)
* [Memory Safety](https://en.wikipedia.org/wiki/Memory_safety)

## Run

### QEMU

[QEMU](https://www.qemu.org/) is requred for dev-mode run

* `cargo xbuild`
* `cargo bootimage`
* `qemu-system-x86_64 -drive format=raw,file=target/x86_64-project_sofia/debug/bootimage-project_sofia.bin`

### Real Machine

`dd if=target/x86_64-project_sofia/debug/bootimage-project_sofia.bin of=/dev/sdX && sync`

Where `sdX` is the device name of your USB stick. Be careful to choose the correct device name, because everything on that device is overwritten.

### Cargo

`cargo xrun`

<a href="https://ibb.co/5n6Ln4z"><img src="https://i.ibb.co/1dLTdQp/26-03-2020-17-40-42.png" alt="26-03-2020-17-40-42" border="0"></a>
