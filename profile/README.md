## Welcome to the riscv-vela project 🙌

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
👀 Contribution guidelines - how do team members dive in?
👩‍💻 Useful resources - where do you keep your docs? Is there anything else the team should know?
🍪 Fun facts - what is your team's favorite snack?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

## 1. Introduction

"Vela" is derived from a constellation name, meaning "the sail that opens a voyage." Vela symbolizes opening a new voyage for Software-Defined Robotics (SDR) through open RISC-V–based system software technologies.

This project aims to establish an open ecosystem for intelligent service robots — Software-Defined Robotics (SDR) — by developing royalty-free, RISC-V–based system software technologies free from dependence on closed foreign computing platforms. Currently, most robot platforms rely on closed ARM- or x86-based systems, which restrict hardware flexibility and impose high licensing costs and vendor lock-in. These constraints hinder innovation, scalability, and autonomous development. This research seeks to build a RISC-V–based SDR computing platform that enables flexible, optimized hardware configurations while reducing dependence on such platforms. As an open instruction set architecture (ISA), RISC-V can be freely extended, customized, and implemented without royalties. Building on this architecture, the project focuses on developing the following core system software technologies:

![Four Goals of riscv-vela project](https://github.com/riscv-vela/.github/blob/main/four_goals.png)
<!--
 - Low Power: Maximize energy efficiency through power management and thermal control
 - High Performance: Integrate multiple AI execution engines and apply multimodel scheduling for performance optimization
 - High Reliability: Support a Trusted Execution Environment (TEE) for confidential computing
 - High Availability: Implement RAS (Error-record Register Interface) for system error prediction, recovery, and continuous operation
-->

By integrating these technologies, the project will build a RISC-V Linux kernel–based system software distribution, incorporating ROS2 (DDS)-based middleware, compilers, profilers, and verification emulators to create an open software platform for intelligent robotics, and AI execution engines prototype.
Ultimately, the goal is to strengthen the domestic RISC-V system software ecosystem, enhance competitiveness in various SDx (On-Device AI) industries, and promote both technological self-reliance and global open-source collaboration.

## 2. License
The Vela project is an open RISC-V–based SDR system software stack that includes multiple open-source components such as the Linux kernel, ROS2, and Ubuntu packages. Therefore, it is distributed under a multi-license open-source scheme, where each component retains its original license.
 - Linux Kernel: GPL-2.0 only
 - ROS2: Apache-2.0 / BSD-3-Clause
 - Ubuntu Packages: GPL, LGPL, MIT, BSD, and other upstream licenses

## 3. Acknowledgement  
This research was supported in part by Institute of Information & communications Technology Planning & Evaluation (IITP) grant funded by the Korea government(MSIT) (No. RS-2024-00459774, RISC-V based system software development for open ecosystem of SDR)

