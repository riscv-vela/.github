## 1. Project Introduction

RISCV-Vela project serves as a collaborative platform for the institutions participating in the research project **“RISC-V-Based System Software Development for an Open SDR Ecosystem”**. It aims to openly release and share the key research outcomes and core software (SW) developed through the project.

The participating institutions include the Electronics and Telecommunications Research Institute (ETRI), Seoul National University (SNU), Yonsei University, Korea University, Chungbuk National University (CBNU), FALINUX, and THIRA Robotics.

The project aims to establish an open ecosystem for intelligent service robots — Software-Defined Robotics (SDR) — by developing royalty-free, RISC-V–based system software technologies free from dependence on closed foreign computing platforms. Currently, most robot platforms rely on closed ARM- or x86-based systems, which restrict hardware flexibility and impose high licensing costs and vendor lock-in. These constraints hinder innovation, scalability, and autonomous development. This research seeks to build a RISC-V–based SDR computing platform that enables flexible, optimized hardware configurations while reducing dependence on such platforms. As an open instruction set architecture (ISA), RISC-V can be freely extended, customized, and implemented without royalties. Building on this architecture, the project focuses on developing the following core system software technologies:

<p align="center">
  <img src="https://github.com/riscv-vela/.github-private/blob/main/profile/design_goals.png"
       alt="Four Goals of riscv-vela project" width="800">
</p>
<!--
 - Low Power: Maximize energy efficiency through power management and thermal control
 - High Performance: Integrate multiple AI execution engines and apply multimodel scheduling for performance optimization
 - High Reliability: Support a Trusted Execution Environment (TEE) for confidential computing
 - High Availability: Implement RAS (Error-record Register Interface) for system error prediction, recovery, and continuous operation
-->

By integrating these technologies, the project will build a RISC-V Linux kernel–based system software distribution, incorporating ROS2 (DDS)-based middleware, compilers, profilers, and verification emulators to create an open software platform for intelligent robotics, and AI execution engines prototype.
Ultimately, the goal is to strengthen the domestic RISC-V system software ecosystem, enhance competitiveness in various SDx (On-Device AI) industries, and promote both technological self-reliance and global open-source collaboration.

## 2. Software Architecture
## Vela-OS / Userspace

> **Base:** Ubuntu 24.04-riscv64
>
> | Component | Category | Repo | Description |
> |-----------|----------|------|-------------|
> | **RISC-V RAS tools · utils** | `RAS` | [vela-apps](https://github.com/riscv-vela/vela-apps) | RAS daemon, logger & devmem utility |
> | **Keystone SDK · runtime · examples** | `TEE` | [vela-apps](https://github.com/riscv-vela/vela-apps) | Enclave app development interface |
> | **Gemmini test code** | `VelaNPU` | [q-vela](https://github.com/riscv-vela/q-vela) | Test code for functional verification of VelaNPU |
> | **Optimized RISC-V Binary** | `Compiler` | [t-vela](https://github.com/riscv-vela/t-vela) | MLIR-based binaries cross-compiled by t-vela |
> | **ROS2 distribution** | `ROS` | [vela-ros](https://github.com/riscv-vela/vela-ros) | vela-ros + RISC-V ported packages |
> | **Performance / power model** | `Power` | [p-vela](https://github.com/riscv-vela/p-vela) | Performance and power monitor for QEMU emulation environment |

## Linux Kernel

> **Base:** Linux Kernel 6.18.0 · **Repo:** [vela-linux](https://github.com/riscv-vela/vela-linux)
>
> | Component | Category | Description |
> |-----------|----------|-------------|
> | **RERI-supporting RAS driver** | `RAS` | RERI error handling, logging, and notification for RISC-V arch. |
> | **linux-keystone-driver** | `TEE` | Keystone host driver |

## Firmware

> **Base:** OpenSBI + EDK2 (UEFI) + U-Boot · **Repo:** [vela-fws](https://github.com/riscv-vela/vela-fws)
>
> | Component | Category | Description |
> |-----------|----------|-------------|
> | **opensbi_RAS agent** | `RAS` | RAS agent handles error-record and reports to the OS using SSE |
> | **opensbi_tee.patch** | `TEE` | WorldGuard request handling / forwarding to SM |
> | **edk2_reri.patch** | `RAS` | Discovers error sources and populates the ACPI HEST table |
> | **Keystone Security Monitor** | `TEE` | Enclave isolation & lifecycle enforcement |

## Hardware Emulator (QEMU)

> **Base:** qemu-system-riscv64 · **Repo:** [q-vela](https://github.com/riscv-vela/q-vela)
>
> | Component | Category | Description |
> |-----------|----------|-------------|
> | **VelaNPU** | `VelaNPU` | Gemmini (systolic array-based NPU) emulation + ternary GEMM support |
> | **RERI-based RAS HW Emulation** | `RAS` | Hardware emulator injecting/generating RERI-compatible hardware error sources |
> | **WorldGuard memory protection** | `TEE` | Hardware memory isolation by world ID (security domain) |
> | **Custom vector instructions** | `VelaVPU` | Custom Vector ISA extensions for RoPE, tokenizer, and PID control |

