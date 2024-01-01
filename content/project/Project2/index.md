---
title: Oblivous Random Access Machine using Red Black trees
summary: Implemented ORAM using Red Black tree as the logical tree underneath, allowing for faster deletions.
tags:
  - Cryptography
date: "2023-03-01"

# Optional external URL for project (replaces project detail page).
# external_link: https://example.org

image:
  caption: Red Black tree ORAM
  focal_point: Smart

# slides = "ORAMSlides".
# slides: example
---

In this project, I successfully developed a sophisticated Oblivious Random Access Machine (ORAM) system based on the Path ORAM architecture. The primary goal of this system is to ensure user privacy by effectively concealing access patterns during data retrieval and manipulation. This is especially crucial in environments where security and privacy are paramount, as it prevents potential attackers from deducing the nature or specifics of user activities based on data access patterns.

The core of the ORAM system utilizes a Red-Black tree structure for its logical organization. The choice of a Red-Black tree is strategic, as it significantly enhances the speed of accessing stored data. Red-Black trees, known for their balanced nature, enable faster data retrieval and updates compared to other binary tree structures. This design decision marks a critical improvement in the efficiency of the ORAM, particularly in environments where rapid data access is essential.

One of the most innovative aspects of this ORAM is its approach to obscuring access patterns. Every time data is accessed, whether for reading or writing, the system executes a series of dummy reads. This approach creates a uniform, or seemingly identical, access pattern for all operations. To an external observer, all actions appear indistinguishable from one another, thereby masking the user's actual data interactions and preserving privacy.

Furthermore, the implementation of this ORAM offers improved performance over previous models, particularly in terms of data deletion efficiency. By opting for Red-Black trees over AVL trees, which are traditionally slower for deletions, the system achieves a notable speed advantage. The entire system is implemented in C++, a language chosen for its execution speed and efficiency. This programming decision is pivotal in ensuring that the ORAM not only maintains high-security standards but also operates with the required swiftness in processing complex data operations. This project stands as a significant contribution to the field of secure data storage and retrieval, paving the way for more secure and efficient data management systems.