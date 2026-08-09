## 1. Relationships among repositories
```mermaid
%%{init: {"theme":"base", "themeVariables": {"fontSize":"12px"}, "flowchart": {"nodeSpacing": 55, "rankSpacing": 75, "padding": 16, "useMaxWidth": false}}}%%

graph TB
    subgraph PKG["Packages / Toolchain"]
        tvela["<b>t-vela</b><br/>
MLIR X-Compiler"]
        click tvela href "https://github.com/riscv-vela/t-vela" "t-vela repository"
        vapps["<b>vela-apps</b><br/>
RAS daemon + <br/>Keystone SDK"]
        click vapps href "https://github.com/riscv-vela/vela-apps" "vela-apps repository"
        vros["<b>vela-ros</b><br/>
ROS 2"]
        click vros href "https://github.com/riscv-vela/vela-ros" "vela-ros repository"
        pvela["<b>p-vela</b><br/>
Perf · Power<br/>
Management"]
        click pvela href "https://github.com/riscv-vela/p-vela" "p-vela repository"
    end

    subgraph OS["OS / Userspace &nbsp;·&nbsp; U-mode"]
        vela["<b>vela</b><br/>
Ubuntu 24.04<br/>
-riscv64 based <br/>
Optimized <br/>
Distribution"]
        click vela href "https://github.com/riscv-vela/vela" "vela repository"
    end

    subgraph KRN["Kernel &nbsp;·&nbsp; S-mode"]
        vlinux["<b>vela-linux</b><br/>
Linux 6.18 <br/>
RERI RAS <br/>
Keystone Driver"]
        click vlinux href "https://github.com/riscv-vela/vela-linux" "vela-linux repository"
    end

    subgraph FW["Firmware &nbsp;·&nbsp; M-mode"]
        fws["<b>vela-fws</b><br/>
OpenSBI · EDK2,<br/>
U-Boot,<br/>
RAS Agent,<br/>
Security Monitor"]
        click fws href "https://github.com/riscv-vela/vela-fws" "vela-fws repository"
    end

    subgraph HW["Hardware Platform"]
        qvela["<b>q-vela</b><br/>
QEMU with<br/>
VelaNPU,<br/>
RERI, and<br/>
WorldGuard"]
        click qvela href "https://github.com/riscv-vela/q-vela" "q-vela repository"
        fvela["<b>f-vela</b><br/>
FPGA with<br/>
Single-core,<br/>
VelaNPU,<br/>
and VelaVPU"]
        click fvela href "https://github.com/riscv-vela/f-vela" "f-vela repository"
        ivela["<b>i-vela</b><br/>
FPGA with<br/>
Multicore,<br/>
Multi VelaNPU/VPU,<br/>
WorldGuard, <br/>
and Ethernet"]
        click ivela href "https://github.com/riscv-vela/i-vela" "i-vela repository"
    end

    tvela -. "compiled <br/>binaries" .-> vela
    vapps -. "install" .-> vela
    vros -. "install" .-> vela
    pvela -. "install" .-> vela

    vela ==>|"includes kernel image"| vlinux
    vlinux ==>|"booted by"| fws
    vlinux -. "SBI ecall · SSE notify" .- fws
    vlinux ==>|"runs on"| HW

    fws ==>|"All runs on"| qvela
    fws ==>|"OpenSBI and <br/>Security Monitor <br/>runs on"| fvela
    fws ==>|"OpenSBI and <br/>Security Monitor <br/>runs on"| ivela

    classDef pkg fill:#fff3e0,stroke:#ef6c00,stroke-width:2px,font-size:18px
    classDef os fill:#e3f2fd,stroke:#1565c0,stroke-width:3px,font-size:18px
    classDef krn fill:#e8f5e9,stroke:#2e7d32,stroke-width:3px,font-size:18px
    classDef fw fill:#f3e5f5,stroke:#6a1b9a,stroke-width:3px,font-size:18px
    classDef hw fill:#eceff1,stroke:#455a64,stroke-width:2px,font-size:18px
    class tvela,vapps,vros,pvela pkg
    class vela os
    class vlinux krn
    class fws fw
    class qvela,fvela,ivela hw
```
Solid line = build/runtime dependency; dashed line = loose reference

## 2. Version pinning

This repository pins each component to a specific commit using Git submodules.

| Repo | 2026-08 | 2026-11 |
|---|---|---|
| [`vela-apps`](https://github.com/riscv-vela/vela-apps) | `v26.08` | `v26.11` |
| [`vela-ros`](https://github.com/riscv-vela/vela-ros) | `v26.08` | `v26.11` |
| [`vela`](https://github.com/riscv-vela/vela) | `v26.08` | `v26.11` |
| [`p-vela`](https://github.com/riscv-vela/p-vela) | — | `v26.11` |
| [`t-vela`](https://github.com/riscv-vela/t-vela) | — | `v26.11` |
| [`vela-fws`](https://github.com/riscv-vela/vela-fws) |`v26.08` | `v26.11` |
| [`q-vela`](https://github.com/riscv-vela/q-vela) | `v26.08` | `v26.11` |
| [`f-vela`](https://github.com/riscv-vela/f-vela) | — | `v26.11` |
| [`i-vela`](https://github.com/riscv-vela/f-vela) | — | `v26.11` |


