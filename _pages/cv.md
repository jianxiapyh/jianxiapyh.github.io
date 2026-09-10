---
layout: single
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

[Download my CV (PDF, September 2026)]({{ '/files/Yihan_Pang_cv_Sept2026.pdf' | relative_url }})

## Research Interests

Systems for spatial computing and embodied AI; scalable infrastructure; algorithm–system co-design; distributed systems.

## Education

- **Ph.D. in Computer Science**, University of Illinois Urbana-Champaign, 2020–May 2027 (anticipated). Advisor: Sarita Adve.
- **M.S. in Computer Engineering**, Virginia Tech, 2016–2019. Advisor: Binoy Ravindran. Thesis: *Leveraging Processor-diversity for Improved Performance in Heterogeneous-ISA Systems*.
- **B.S. in Computer Engineering**, Virginia Tech, 2011–2015. Minors: Mathematics and Cybersecurity.

## Research Experience

### NVIDIA — Ph.D. Intern

*Santa Clara, CA · May–August 2026*

Developed and scaled ML training and data infrastructure for the XR team's 3D hand reconstruction models, spanning synthetic data generation, preprocessing, storage and loading, sampling, and targeted data curation. Improved generation speed by **1.6×** and preprocessing speed by **2.6×**, saving approximately **20,000 A100 GPU-hours** within a few days of large-scale generation. Built tooling to turn observed model failures into reusable synthetic training data.

### University of Illinois Urbana-Champaign — Research Assistant

*Champaign, IL · 2020–present · Advisor: Sarita Adve*

Design energy-efficient systems for real-time spatial computing, with collaboration with Meta Reality Labs since 2024.

- **Boba:** A scalable system for physics-based Gaussian digital twins, achieving over 10× single-instance speedup, 3,310 FPS aggregate batched throughput, and 22.2% lower edge-device incremental power through distributed execution.
- **Ada:** A distributed, power-aware scene provider that reduces device-side incremental power by 24% while maintaining comparable latency and scene fidelity.
- Collaborate on visual–inertial odometry, scene reconstruction, and task-aware real-time depth estimation, and integrate research systems into the open-source ILLIXR testbed.

### Virginia Tech — Research Assistant

*Blacksburg, VA · 2016–2019 · Advisor: Binoy Ravindran; additional research with X. Jian, 2018–2019*

Studied heterogeneous processor and ISA designs, developing SIMD migration support, LLVM compiler passes, Linux kernel changes, and scheduling techniques for heterogeneous systems. Also quantified memory underutilization in HPC systems and developed architectural and OS support to improve memory utilization and performance.

## Publications

See my [selected publications]({{ '/' | relative_url }}#selected-publications), [other publications]({{ '/' | relative_url }}#other-publications), and [manuscripts under review]({{ '/' | relative_url }}#manuscripts-under-review). The downloadable CV includes the full publication list.

## Technical Skills

- **Programming:** C/C++, Python, Bash.
- **ML and GPU computing:** PyTorch, CUDA, NVIDIA Warp, Nsight Compute.
- **Systems and tools:** ILLIXR, GStreamer/FFmpeg, LLVM.

## Honors and Awards

- Best Paper Award, ISMAR 2025 — Ada.
- Best Paper Award, IISWC 2021; IEEE Micro Top Pick — ILLIXR.
- Full Tuition Scholarship, Virginia Tech, 2016–2019.
- Dean's List, Virginia Tech, 2011–2015.
