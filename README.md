# Ákos Arinton

**Software Development Engineer @ AWS** · Systems Performance, Distributed Systems & Database Internals

[LinkedIn](https://linkedin.com/in/arinton-akos) · [Email](mailto:arintonakos@gmail.com) · [Stack Overflow](https://stackoverflow.com/users/arintonakos) · [Work GitHub](https://github.com/arintonakos1)

Focused on low-level performance engineering, runtime/GC optimization (JVM & .NET), storage engines, program analysis tooling, and high-throughput cloud infrastructure.

---

## Experience

**AWS** — *Software Development Engineer* (`09/2024 – Present`)
- Engineered PostgreSQL runtime query-generation optimizations (row-comparison B-tree index seeks), achieving a **7,161x speedup** (`3,115 ms → 0.4 ms`) on critical positioning queries across modernized workloads.
- Eliminated cold-start database latency (`158 s → 0.4 ms`) via `pg_prewarm` buffer management, reduced batch processing from `11 min → 3 s` (**220x**), and cut report generation latency **13x** via multi-layer caching.
- Eliminated JVM GC bottlenecks, refactored hot regex/string paths, and implemented HikariCP connection pooling with cross-transaction cursor persistence (`WITH_HOLD`).
- Architected an IDE-agnostic autonomous regression-resolution pipeline (**MCP server + static code analysis / Test Impact Analysis** using call graphs and class hierarchies) integrated with distributed AWS test execution.
- Built a binary **TN5250/TN3270** protocol parser with an HTML5 Canvas terminal renderer, and led root-cause investigations resolving 30+ critical/blocker runtime defects.

**Egnosis** — *Software Engineer* (`04/2022 – 09/2024`)
- Built a multithreaded **C++ 2D bin-packing optimizer** (Genetic Algorithms) for CNC manufacturing, increasing raw material utilization from **63% to 86%**.
- Architected a distributed, high-volume image processing and search pipeline (RabbitMQ, GPU-accelerated Python workers, Elasticsearch).
- Engineered standalone Raspberry Pi edge devices with real-time telemetry, local Wi-Fi diagnostics, and automated cloud sync.

---

## Selected Systems & Performance Work

**[DataVo-DBMS](https://github.com/ArintonAkos/DataVo-DBMS) & DataVo-Sync** — *Embedded SQL/Vector Engine & PostgreSQL CDC Sync (C# / .NET)*
- Zero-dependency, **Native-AOT** relational and vector database in pure C# (.NET 10 / `netstandard2.1`) with B+Tree/LSM storage, MVCC snapshot isolation, ADO.NET & EF Core providers, HNSW vector indexing, and WebAssembly support.
- Built **Roslyn compile-time LINQ interceptors** (`[InterceptsLocation]`) and zero-allocation `ref struct RowRef` scans — cutting 200k-row query garbage from `22.4 MB → 0 B` and accelerating scans up to **21x** (`5.1–5.3 µs / 0 B` for 100-row PK range aggregates).
- Engineered **DataVo-Sync**, a custom zero-dependency binary PostgreSQL `pgoutput` logical replication client and multi-tenant sync hub with SIMD CRC32C, HLC versioning, and RLS claim evaluation (`1.15–1.34 ms` p50 live PG17 commit-to-replica propagation; 3,223+ core tests & 316/316 live PG17 sync tests).

**Open-Source Rust Performance Contributions** — *[FilmCraft](https://github.com/storytold/filmcraft) & [PhotoCraft](https://github.com/storytold/photocraft) (74k+ ★)*
- **[FilmCraft PR #3379](https://github.com/storytold/filmcraft/pull/3379)** — Architected the `filmcraft-simd` crate with NEON (`aarch64`) and SSE2 (`x86_64`) kernels across AV1, H.264, HEVC, VP8, and VP9 decoders, verified bit-exact across 3,688 CI tests and outperforming `ffmpeg` on multithreaded H.264, HEVC, and VP9.
- **[FilmCraft PR #3601](https://github.com/storytold/filmcraft/pull/3601)** — Implemented full multithreaded pure-Rust VP8 decoding (up to 12 frames in flight), reaching **1,538 fps** at 1080p and beating multithreaded `ffmpeg`.
- **[PhotoCraft PR #10126](https://github.com/storytold/photocraft/pull/10126) & [PR #7566](https://github.com/storytold/photocraft/pull/7566)** — Built a CPU compositor prefix cache delivering a **56x redraw speedup** (`563 ms → 10 ms`) and GPU multi-layer compositing delivering a **4x speedup** (`111 ms → 28 ms`).

**[fnblur](https://github.com/ArintonAkos/fnblur)** — *SIMD Image Processing Kernels (C++ / ARM NEON / Python)*
- Custom C++ Python extension (`pybind11`) with hand-tuned ARMv8 NEON intrinsics, zero-copy memory handling, and cache-resident multithreading (~25x lower single-image latency vs. PyTorch MPS; 3x higher per-iteration throughput vs. OpenCV).

**[x86-assembly-io-library](https://github.com/ArintonAkos/x86-assembly-io-library)** — *Zero-Dependency Assembly I/O (NASM x86)*
- Pure x86 Assembly integer and binary I/O library without standard libraries, implementing manual 64-bit arithmetic on 32-bit `EDX:EAX` register pairs with Carry Flag (`CF`) error propagation.

---

## Core Stack

| Area | Technologies |
| :--- | :--- |
| **Languages** | `C++` · `C` · `Rust` · `Go` · `C#` · `Java` · `Python` · `x86 / ARM Assembly` |
| **Performance & Internals** | `SIMD (ARM NEON / AVX2 / SSE2)` · `JVM & .NET GC Tuning` · `Roslyn / Static Analysis` · `Storage Engines (LSM, B+Tree, MVCC)` · `Profiling (perf, gdb, BenchmarkDotNet)` |
| **Cloud & Data** | `AWS` · `Kubernetes` · `Docker` · `PostgreSQL (pgoutput / Internals)` · `SQLite` · `Redis` · `Elasticsearch` · `Linux` · `CMake` |

---

## Education & Prior Research

- **B.Sc. in Computer Science**, Babeș-Bolyai University — *1st Place Best Thesis* (Semantic Image Synthesis for Autonomous Driving, sponsored by SoftServe).
- **Research Collaborator (Voluntary)**, University of Hamburg — Privacy-preserving federated latent diffusion models for diagnostic imaging across hospital data silos.

---
*All open-source projects, benchmarks, and views here are my own and do not represent my employer.*
