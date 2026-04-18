---
Theme:
  - "[[Computer science]]"
---
##  x86 Processor (32-bit)

![[processor.jpg]]

### Registers (architectural state)
**General‑purpose 32‑bit registers:** EAX, EBX, ECX, EDX, ESI, EDI, EBP, ESP
**Instruction pointer:** EIP
**Flags register:** EFLAGS
**Segment registers:** CS, DS, ES, FS, GS, SS
**Control registers:** CR0–CR4, CR8 (64‑bit mode)

>These registers are held inside the core itself and are accessible in a single cycle; they are **not** part of the cache hierarchy but give context for where cached data eventually lands.

### L1 Cache (on‑core, Harvard architecture)
**Instruction cache:** 16 KB, 4‑way set associative, ~3 cycle latency
**Data cache:** 16 KB, 4‑way set associative, ~3 cycle latency

### L2 Cache (on‑die, unified)
**Unified cache:** 256 KB, 8‑way set associative, ~10–12 cycle latency

### L3 Cache (on‑die, shared)
**Unified cache:** 8 MB, 16‑way set associative, ~30–40 cycle latency

## Main Memory (DRAM) 
- **Typical capacity:** 8–64 GB
- **Latency (from core):** 200–300 cycles (~60–90 ns)
- **Bandwidth:** Depends on memory channels and speed (e.g., DDR4‑3200 ≈ 25 GB/s per channel)