# GNSSForge

**A Resource-Efficient FPGA Accelerator for Software-Defined GNSS Receivers**

[![License: BSD-2-Clause](https://img.shields.io/badge/License-BSD--2--Clause-blue.svg)](LICENSE)
[![Target: Zynq-7020](https://img.shields.io/badge/Target-Zynq--7020-orange.svg)](docs/ARCHITECTURE.md)
[![Status: Active Development](https://img.shields.io/badge/Status-Active-green.svg)](ROADMAP.md)

---

## 🎯 Overview

**GNSSForge** is an open-source, resource-efficient FPGA accelerator for Global Navigation Satellite System (GNSS) receivers. It implements the core baseband processing—acquisition, tracking, and correlation—in programmable logic, enabling real-time multi-channel GNSS reception on low-cost SoC-FPGA platforms.

The design philosophy prioritizes **resource efficiency**: maximizing the number of tracking channels per LUT, DSP slice, and BRAM block, without sacrificing tracking performance.

### Key Features

- 🚀 **32+ tracking channels** on a single Zynq-7020 (ZedBoard)
- ⚡ **Hardware closed-loop tracking** (PLL/DLL filters in FPGA, <1 ms latency)
- 🎯 **Time-multiplexed acquisition engine** (shared FFT across all PRNs)
- 📡 **Multi-GNSS ready**: GPS L1 C/A (primary), extensible to Galileo E1, BeiDou B1I
- 🔌 **AXI4-compliant interface** for seamless ARM integration
- 🧪 **Python golden model** for bit-exact RTL verification
- 📖 **Fully open-source** with complete documentation

### Target Platforms

| Phase | Platform | FPGA | Status |
|-------|----------|------|--------|
| Phase 1–6 | **ZedBoard** | Zynq-7020 (53K LUTs, 220 DSP48) | 🚧 In progress |
| Phase 7+ | **ADRV9361-Z7035** | Zynq-7035 (106K LUTs, 900 DSP48) | 📋 Planned |

---

## 🏗️ Architecture
