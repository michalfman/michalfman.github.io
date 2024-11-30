---
title: "FliT: A Library for Simple and Efficient Persistent Algorithms"
collection: publications
authors_before_me: Yuanhao Wei, Naama Ben-David
author_me: Michal Friedman
authors_after_me: Guy E. Blelloch, Erez Petrank
date: 2022-04-05
venue: 'PPoPP 2022: Principles and Practice of Parallel Programming'
---
[Paper](https://dl.acm.org/doi/pdf/10.1145/3503221.3508436)

Abstract: Non-volatile random access memory (NVRAM) offers byte-addressable persistence at speeds comparable to DRAM. However, with caches remaining volatile, automatic cache evictions can reorder updates to memory, potentially leaving persistent memory in an inconsistent state upon a system crash. Flush and fence instructions can be used to force ordering among updates, but are expensive. This has motivated significant work studying how to write correct and efficient persistent programs for NVRAM.
In this paper, we present FliT, a C++ library that facilitates writing efficient persistent code. Using the library’s default mode makes any linearizable data structure durable with minimal changes to the code. FliT avoids many redundant flush instructions by using a novel algorithm to track dirty cache lines. It also allows for extra optimizations, but achieves good performance even in its default setting.
To describe the FliT library’s capabilities and guarantees, we define a persistent programming interface, called the P-V Interface, which FliT implements. The P-V Interface captures the expected behavior of code in which some instructions’ effects are persisted and some are not. We show that the interface captures the desired semantics of many practical algorithms in the literature.
We apply the FliT library to four different persistent data structures, and show that across several workloads, persistence implementations, and data structure sizes, the FliT library always improves operation throughput, by at least 2.1× over a naive implementation in all but one workload.
