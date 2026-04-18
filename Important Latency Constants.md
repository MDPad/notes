---
Theme:
  - "[[Memory types]]"
---
![[Memory Caching.png]]

|  1 cycle                 | = 1 / CPU frequency               |
| ------------------------ | --------------------------------- |
| 1 / 3 GHz                | ≈ 0.3 ns                          |
| L1 cache reference       | 0.5 ns                            |
| Branch mispredict        | 5 ns   // failed if()             |
| L2 cache reference       | 7 ns                              |
| Mutex lock/unlock        | 25 ns                             |
| Main memory reference    | 100 ns   // throughput 10‑50 GB/s |
| Compress 1 KB with Zippy | 3,000 ns                          |
| Send 1 KB over 1 Gbps    | 10,000 ns                         |
| Read 4 KB random SSD     | 150,000 ns                        |
| Read 1 MB sequential RAM | 250,000 ns                        |
| Round‑trip same DC       | 500,000 ns                        |
| Read 1 MB sequential SSD | 1,000,000 ns                      |
| HDD seek                 | 10,000,000 ns                     |
| Read 1 MB sequential HDD | 20,000,000 ns                     |
| Packet CA→NL→CA          | 150,000,000 ns                    |
