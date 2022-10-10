---
title: "Efficient Logging in Non-Volatile Memory by Exploiting Coherency Protocols"
collection: publications
authors_before_me: Nachshon Cohen
author_me: Michal Friedman
authors_after_me: James R. Larus
date: 2017
venue: 'OOPSLA 2017: Proceedings of the ACM on Programming Languages'
---
[Paper](https://dl.acm.org/doi/pdf/10.1145/3133891)

Abstract: Non-volatile memory (NVM) technologies such as PCM, ReRAM and STT-RAM allow processors to directly write values to persistent storage at speeds that are significantly faster than previous durable media such as hard drives or SSDs. Many applications of NVM are constructed on a logging subsystem, which enables operations to appear to execute atomically and facilitates recovery from failures. Writes to NVM, however, pass through a processor’s memory system, which can delay and reorder them and can impair the correctness and cost of logging algorithms.
Reordering arises because of out-of-order execution in a CPU and the inter-processor cache coherence protocol. By carefully considering the properties of these reorderings, this paper develops a logging protocol that requires only one round trip to non-volatile memory while avoiding expensive computations. We show how to extend the logging protocol to building a persistent set (hash map) that also requires only a single round trip to non-volatile memory for insertion, updating, or deletion.
