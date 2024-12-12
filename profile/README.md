#  RISC-V based system software development for open ecosystem of SDR
<br>

## What is Vela
 * Development of open system software technology to support a low-power, high-efficiency, high-reliability, and high-availability execution environment by linking RISC-V hardware expansion technology to strengthen the open SDR software ecosystem.

# Overview
## System Architecture for Intelligent SDR Applications with RISC-V

This diagram represents a comprehensive system architecture for intelligent SDR (Software Defined Radio) applications leveraging RISC-V. The architecture consists of three main layers: **Middleware**, **Linux Kernel**, and **Verification Environment**.

### Middleware
The middleware layer focuses on:
- RISC-V compiler optimization and ISA-based load balancing.
- Resource monitoring and profiling for system performance.
- AI model execution and SDR application performance optimization.
- System resource and power management tools.

### Linux Kernel
The Linux Kernel layer is divided into four key subsystems:
-  **Low-Power Kernel**:
   - Power analysis, DVFS (Dynamic Voltage-Frequency Scaling), and thermal management.
-  **High-Efficiency Kernel**:
   - AI engine scheduling, multi-model optimization, and efficient message communication.
-  **High-Availability Kernel**:
   - RAS (Reliability, Availability, and Serviceability) event handling and error recovery.
-  **Trusted Execution Manager**:
   - Secure AI engine execution, memory isolation, and trusted execution environment support.

### Verification Environment
The verification environment provides:
- RISC-V ISA extensions and enhanced AI engine performance.
- Support for power optimization, reliability, and scalability.
- Tools for validating system integrity and ensuring robust execution environments.

This architecture enables a highly reliable, scalable, and efficient system for high-performance SDR applications.


![SDR_RISCV_Res](https://github.com/riscv-vela/.github/blob/main/sdr_riscv_res.png?raw=true)

### Operating System
 * Development and integration of a system software distribution that includes a RISC-V-supported Linux kernel, system libraries, and various management tools to enable seamless execution of intelligent SDR applications.
   
### Verification Environment
 * Development of an emulator/simulator/FPGA-based environment for the development and functionality/performance verification of RISC-V ISA and non-ISA extension features.

### Low Power
 * Development of static/dynamic power-saving and thermal management technologies based on performance monitoring information in heterogeneous environments composed of RISC-V cores and multiple AI execution engines.

### High Efficiency
 * Development of high-efficiency computing technologies, including ISA-extended AI execution engines for SDR, multi-model integrated scheduling for intelligent robotic applications, and power/thermal-aware scheduling.

### High Reliability
 * Development of error analysis/reporting capabilities based on RERI (RAS Error-record Register Interface) and technologies supporting error prediction/isolation to enhance system availability during fault scenarios.

### High Availability
 * Development of error analysis/reporting capabilities based on RERI (RAS Error-record Register Interface) and technologies supporting error prediction/isolation to enhance system availability during fault scenarios.

### Toolchain
 * Development of toolchain tools, including compilers for generating code for AI execution engines and extended ISA support for low-power, high-efficiency, high-reliability, and high-availability features, along with a profiler for performance optimization.

### Application Optimization
 * Development of application optimization scenarios based on SDR application characteristic analysis and application optimization technologies to support accelerated message communication between intelligent SDR applications.

<br>
