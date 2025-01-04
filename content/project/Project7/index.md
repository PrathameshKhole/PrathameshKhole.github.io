---
title: The Octo-Wumpus Protocol, An approach to make lottery scheduling more fair
summary: Proposed an enhanced scheduling algorithm to improve fairness in lottery scheduling using the Octo-Wumpus protocol.
tags:
  - Systems
date: "2024-03-15"

# Optional external URL for project (replaces project detail page).
external_link: https://github.com/SanyaSriv/Octo-Wumpus-Scheduler.git

image:
  caption: Octo-Wumpus Art
  focal_point: Smart

# slides = "ORAMSlides".
# slides: example
---

The **Octo-Wumpus Protocol** is an innovative enhancement to the classic lottery scheduling algorithm, designed to achieve greater fairness in process scheduling. While lottery scheduling provides proportional fairness based on ticket allocation, it suffers from stochastic behavior that may lead to starvation for some processes. The Octo-Wumpus protocol introduces two key approaches to mitigate this issue:

1. **Queue-Based Scheduling**: Implements a deterministic second-level scheduler that prioritizes starved processes in subsequent epochs to ensure fairness.
2. **Alpha-Inflation Protocol**: Dynamically adjusts the ticket allocation of starved processes by inflating their ticket count, increasing their chances of selection in future epochs while maintaining the probabilistic nature of lottery scheduling.

The project involved rigorous experimentation with multithreaded applications, including parallel merge sort, multithreaded DFS, and file operations. The results demonstrated significant improvements in fairness while maintaining efficiency. Future work includes optimizing performance by transitioning to a lower-level language and exploring additional features such as ticket taxation and dynamic user interfaces.

This work contributes to the field of operating systems by providing a novel solution to enhance fairness in process scheduling without sacrificing the flexibility of lottery scheduling. The source code and detailed logs of the experiments are available in the [GitHub repository](https://github.com/SanyaSriv/Octo-Wumpus-Scheduler).
