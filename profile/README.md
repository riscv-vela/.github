## 1. Introduction
**Vela** — named after the constellation, *"the sail that opens a voyage"* — is an open-source
system software stack for **RISC-V computing platforms**, with
**Software-Defined Robotics (SDR)** as its leading application domain.

Edge systems today rest on closed ARM and x86 platforms that impose licensing costs, vendor
lock-in, and rigid hardware choices. Vela offers a royalty-free alternative: an open ISA, an
open toolchain, and an openly developed stack spanning hardware models, firmware, kernel,
distribution, and applications — with RAS, TEE, and NPU acceleration built in across layers.

Every layer is released publicly and developed in the open. Our goal is to grow the RISC-V
ecosystem, keeping each component reusable across robotics, industrial, automotive, and
other edge workloads.

[Open Source Summit Korea 2026 Pamphlet](https://github.com/riscv-vela/.github/blob/main/profile/riscv-vela_OSS_Korea_en.pdf)

## 2. Overview of repositories

| Repository | Role | Layer | Language | Status |
|---|---|---|---|---|
| [`vela-apps`](https://github.com/riscv-vela/vela-apps) | I/F, Runtime/SDK | System SW | C/C++ | Public |
| [`vela-ros`](https://github.com/riscv-vela/vela-ros) | ROS2 | System SW | C | Public |
| [`vela`](https://github.com/riscv-vela/vela) | Linux Distribution | OS | Shell | Public|
| [`vela-linux`](https://github.com/riscv-vela/vela-linux) | Linux Kernel + Driver | OS | C | Public|
| [`p-vela`](https://github.com/riscv-vela/.github/blob/main/profile/p-vela.md) | Power Management | System SW | Python | $\color{gray}\text{Planned}$ |
| [`t-vela`](https://github.com/riscv-vela/.github/blob/main/profile/t-vela.md) | Cross AI Compiler | Tools | C++ | $\color{gray}\text{Planned}$ |
| [`vela-fws`](https://github.com/riscv-vela/vela-fws) |Bootloader/Monitor | FW | C | Public |
| [`q-vela`](https://github.com/riscv-vela/q-vela) | RISC-V SW Emulation-QEMU | HW | C | Public |
| [`f-vela`](https://github.com/riscv-vela/.github/blob/main/profile/f-vela.md) | RISC-V FPGA| HW | Chisel, Scala, C++ | $\color{gray}\text{Planned}$ |
| [`i-vela`](https://github.com/riscv-vela/.github/blob/main/profile/i-vela.md) | Enhanced RISC-V FPGA| HW | Chisel, Scala, C++ | $\color{gray}\text{Planned}$ |

## 3. Relationships of repositories
<p align="center">
  <img src="https://github.com/riscv-vela/.github/blob/main/profile/repo_arch.png"
       alt="Relationships among repositories" width="600">
</p>

See [Details of repo.](./repo.md) for **relationships**, **version pinning**, **Getting Started** and **contribution**.

## 4. License
The Vela project is an open RISC-V–based SDR system software stack that includes multiple open-source components such as the Linux kernel, ROS2, and Ubuntu packages. Therefore, it is distributed under a multi-license open-source scheme, where each component retains its original license.
 - Linux Kernel: GPL-2.0 only
 - ROS2: Apache-2.0 / BSD-3-Clause
 - Ubuntu Packages: GPL, LGPL, MIT, BSD, and other upstream licenses

## 5. Acknowledgement  
This research was supported in part by Institute of Information & communications Technology Planning & Evaluation (IITP) grant funded by the Korea government(MSIT) (No. RS-2024-00459774, [RISC-V based system software development for open ecosystem of SDR](./vela_project.md))

