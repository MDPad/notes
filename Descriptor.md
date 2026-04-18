---
Theme:
  - "[[Computer science]]"
---
#### Descriptor

A segment descriptor is an **8‑byte (64‑bit)** record that tells the CPU where a segment begins (Base), how large it is (Limit), and under what conditions it can be used (Type/DPL/Flags).

**Key fields at a glance**
- **Base address** — linear start address of the segment.
- **Segment limit** — size of the segment; unit picked by the **G** bit (bytes vs pages).
- **Purpose flags** (Type, DPL, P, etc.) — control read/write/execute rights and privilege level.

---

 - `Segment limit` (20 bits) — size of the segment. Bit 55 **G** selects granularity:
	- 0 → limit measured in **bytes**
    - 1 → limit measured in **pages** (page size usually 4 KB)
- Bits 41‑43 describe segment type:
    - `000` — data segment, read‑only
    - `001` — data segment, read/write
    - `010` — stack segment, read‑only
    - `011` — stack segment, read/write
    - `100` — code segment, execute‑only
    - `101` — code segment, read/execute