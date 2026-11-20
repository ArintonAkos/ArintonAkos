# Ákos Arinton

**Software Development Engineer @ AWS** · Systems Performance, Distributed Systems & Database Internals

[LinkedIn](https://linkedin.com/in/arinton-akos) · [Email](mailto:arintonakos@gmail.com) · [Stack Overflow](https://stackoverflow.com/users/arintonakos) · [Work GitHub](https://github.com/arintonakos1)

Focused on low-level performance engineering, runtime/GC optimization (JVM & .NET), storage engines, and high-throughput cloud infrastructure.

---

## Experience

**AWS** — *Software Development Engineer* (`09/2024 – Present`)
- Optimized critical infrastructure paths, achieving **multi-thousand-fold query performance improvements**.
- Eliminated garbage collection bottlenecks in high-throughput services, substantially reducing tail latency.
- Resolved database execution bottlenecks through index redesign, query restructuring, and connection pooling.
- Designed modernization strategies for legacy enterprise systems.

**Egnosis** — *Software Engineer* (`04/2022 – 09/2024`)
- Implemented C++ optimization algorithms for manufacturing resource allocation.
- Architected distributed data ingestion and high-volume real-time pipelines backed by Elasticsearch.
- Optimized production inference latency for automated classification pipelines.

---

## Selected Systems & Performance Projects

**[DataVo-DBMS](https://github.com/ArintonAkos/DataVo-DBMS)** — *Embedded SQL & Vector Database Engine (C# / .NET)*
- Relational and vector database built from scratch in pure managed C# with zero native dependencies.
- Features an **AST-first query execution pipeline**, custom **B+Tree and LSM-tree storage engines**, **SIMD-vectorized execution**, incremental joins, and native **HNSW** vector indexing.

**[fnblur](https://github.com/ArintonAkos/fnblur)** — *SIMD Image Processing Kernels (C / C++ / ARM NEON)*
- Low-level Gaussian blur and grayscale kernels written with **ARM NEON SIMD intrinsics**.
- Multithreaded execution using barrier synchronization, with systematic SISD vs. SIMD benchmarks against OpenCV.

**[x86-assembly-io-library](https://github.com/ArintonAkos/x86-assembly-io-library)** — *Zero-Dependency Assembly I/O (NASM x86)*
- Pure x86 Assembly integer and binary I/O library built without standard libraries.
- Implements manual 64-bit integer arithmetic on 32-bit `EDX:EAX` register pairs with Carry Flag (`CF`) error propagation.

---

## Core Stack

| Area | Technologies |
| :--- | :--- |
| **Languages** | `C++` · `C` · `Rust` · `Go` · `C#` · `Java` · `Python` · `x86 / ARM Assembly` |
| **Performance & Runtime** | `SIMD (ARM NEON / Hardware Intrinsics)` · `JVM & .NET GC Tuning` · `Query & Index Optimization` · `Profiling & Benchmarking` · `Linux` |
| **Cloud & Infrastructure** | `AWS` · `Kubernetes` · `Docker` · `PostgreSQL` · `SQLite` · `Redis` · `Elasticsearch` · `CMake` · `CI/CD` |

---

## Education & Prior Research

- **B.Sc. in Computer Science**, Babeș-Bolyai University — *1st Place Best Thesis* (Semantic Image Synthesis for Autonomous Driving, sponsored by SoftServe).
- **Research Collaborator (Voluntary)**, University of Hamburg — Privacy-preserving federated latent diffusion models for diagnostic imaging across hospital data silos.

---
*All open-source projects, benchmarks, and views here are my own and do not represent my employer.*
