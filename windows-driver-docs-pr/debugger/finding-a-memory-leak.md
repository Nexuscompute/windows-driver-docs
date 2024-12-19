---
title: Find a Memory Leak
description: Provides information about how to find memory leak.
keywords: ["memory leak", "memory leak, debugging"]
ms.date: 12/06/2024
---

# Find a memory leak

A memory leak occurs when a process allocates memory from the paged or nonpaged pools, but doesn't free the memory. As a result, these limited pools of memory are depleted over time, causing Windows to slow down. If memory is completely depleted, failures may result.

## In this section

| Article | Description |
|---|---|
| [Use perfmon to determine whether a memory leak exists](determining-whether-a-leak-exists.md) | Describes a technique you can use if you aren't sure whether there's a memory leak on your system. |
| [Finding a Kernel-Mode Memory Leak](finding-a-kernel-mode-memory-leak.md) | Describes how to find a leak that is caused by a kernel-mode driver or component. |
| [Finding a User-Mode Memory Leak](finding-a-user-mode-memory-leak.md) | Describes how to find a leak that is caused by a user-mode driver or application. |
