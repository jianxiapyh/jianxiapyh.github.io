---
title: "Cross-ISA Execution of SIMD Regions for Improved Performance"
collection: publications
permalink: /publication/2019-systor
excerpt: 'This paper investigates the effectiveness of executing SIMD workloads on multiprocessors with heterogeneous ISA cores'
date: 2019-04-14
venue: 'ACM SYSTOR 2019'
paperurl: 'http://jianxiapyh.github.io/files/yihan_systor19.pdf'
---

Abstract
======
We investigate the effectiveness of executing SIMD workloads
on multiprocessors with heterogeneous Instruction
Set Architecture (ISA) cores. Heterogeneous ISAs offer an
intriguing clock speed/parallelism tradeoff for workloads
with frequent usage of SIMD instructions. We consider dynamic
migration of SIMD and non-SIMD workloads across
ISA-different cores to exploit this trade-off. We present the
necessary modifications for a general compiler/run-time infrastructure
to transform the dynamic program state of SIMD
regions at run-time from one ISA format to another for crossISA
migration and execution. Additionally, we present a
SIMD-aware scheduling policy that makes cross-ISA migration
decisions that improves system throughput. We prototype
a heterogeneous-ISA system using an Intel Xeon x86-64
server and a Cavium ThunderX ARMv8 server and evaluate
the effectiveness of our infrastructure and scheduling policy.
Our results reveal that cross-ISA execution migration
within SIMD regions can yield throughput gains up to 36%
compared to traditional homogeneous ISA systems

[Download paper here](http://jianxiapyh.github.io/files/yihan_systor19.pdf)

