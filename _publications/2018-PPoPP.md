---
title: "A Persistent Queue for Non-Volatile Memory"
collection: publications
authors_before_me:
author_me: Michal Friedman
authors_after_me: Maurice Herlihy, Virendra Marathe, Erez Petrank
date: 2018
venue: 'PPoPP 2018: Principles and Practice of Parallel Programming'
---
[Paper](https://dl.acm.org/doi/pdf/10.1145/3200691.3178490)

Abstract: Non-volatile memory is expected to coexist with (or even displace) volatile DRAM for main memory in upcoming architectures. 
This has led to increasing interest in the problem of designing and specifying durable data structures that can recover from system crashes. 
Data structures may be designed to satisfy stricter or weaker durability guarantees to provide a balance between the strength of the provided guarantees and performance overhead.  
This paper proposes three novel implementations of a concurrent lock-free queue. 
These implementations illustrate algorithmic challenges in building persistent lock-free data structures with different levels of durability guarantees. 
In presenting these challenges, the proposed algorithmic designs, and the different durability guarantees, we hope to shed light on ways to build a wide variety of durable data structures. 
We implemented the various designs and compared their performance overhead to a simple queue design for standard (volatile) memory.
