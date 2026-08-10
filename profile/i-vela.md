> [!NOTE]
> **Coming soon.** F-Vela is currently under internal development and will be
> released publicly as part of the [riscv-vela](https://github.com/riscv-vela/vela)
> project. Stay tuned for the initial public release.

# i-vela : RICS-V based FPGA Test Platform through integrating Vela

"i-vela" is a project for integrating Vela system on FPGA Test Platform. There are several repository for Vela project. "f-vela" is a repository including NPU/VPU for FPGA Test Platform using FireSim. "q-vela" is a repository for emulating Vela on QEMU, and "t-vela" is for developing compiler toolchain. 'i-vela' integrates them on FPGA Test Platform(proFPGA or VCU118)

## Project Overview
The goals of i-vela are:
- To provide a testbed where a RISC-V SoC runs on FPGA and NPU/VPU can be
  validated on real hardware
- To extend the single-core + single NPU/VPU configuration of f-vela into a
  multi-core RISC-V SoC with multiple NPU/VPU accelerators
- To add Ethernet support on top of the existing f-vela hardware, enabling
  network connectivity for the RISC-V SoC
- To support two FPGA environments:
  - Xilinx VCU118
  - proFPGA with Xilinx XCVU19P
