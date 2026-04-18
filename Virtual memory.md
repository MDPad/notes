---
Theme:
  - "[[Computer science]]"
---
- Memory is divided into **pages**.
- A page may reside in RAM or on external storage.
- Translation between virtual and physical addresses uses special tables: **PGD** (Page Global Directory), **PMD** (Page Middle Directory), **PTE** (Page Table Entry). The `PTE` holds physical page addresses.
- To speed up translation, the CPU caches page‑table entries in the **TLB** (Translation Lookaside Buffer).
- If an address can’t be translated via the TLB, the CPU walks the page tables and tries to load the PTE and after that TLB. If that fails, it raises a **Page Fault**.
- The Page‑Fault handler — part of the OS virtual‑memory subsystem — can load the required page from external storage into RAM.