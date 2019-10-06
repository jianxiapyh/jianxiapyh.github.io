---
title: "Quantifying Memory Underutilization in HPC Systems and Using it to Improve Performance via Architecture Support"
collection: publications
permalink: /publication/2019-micro
excerpt: 'This paper investigates memory underutilization problem in HPC system and purposes new microarchitectural techniques to improve performance'
date: 2019-07-22
venue: 'IEEE/ACM MICRO 2019'
paperurl: 'http://jianxiapyh.github.io/files/yihan_micro19.pdf'
---

Abstract
======
A system’s memory size is often dictated by worst-case workloads
with highest memory requirements; this causes memory to be underutilized
in the common case when the system is not running its
worst-case workloads. Cognizant of this memory underutilization
problem, many prior works have studied memory utilization and
explored how to improve it in the context of cloud.
In this paper, we perform the first large-scale study of systemlevel
memory utilization in the context of HPC systems; through
seven million machine-hours of measurements across four HPC
systems, we find memory underutilization in HPC systems is much
more severe than in cloud. Subsequently, we also perform the first
exploration of architectural techniques to improve memory utilization
specifically for HPC systems. We propose exposing each
compute node’s currently unused memory to its CPU(s) via novel
architectural support for OS. This can enable many new microarchitecture
techniques that use the abundant free memory to boost
microarchitecture performance transparently without requiring
any user code modification or recompilation; we refer to them
as Free-memory-aware Microarchitecture Techniques (FMTs). We
then present a detailed example of an FMT – Free-memory-aware
Memory Replication (FMR). On average across five HPC benchmark
suites, FMR provides 13% performance and 8% system-level
energy improvement compared to a highly optimized baseline representative
of modern memory systems. To check the performance
benefits our simulation reports, we emulated FMR in a real system
and found close corroboration between simulation results and
real-system emulation results. The paper ends by discussing other
possible FMTs and applicability to other types of systems.

[Download paper here](http://jianxiapyh.github.io/files/yihan_micro19.pdf)

