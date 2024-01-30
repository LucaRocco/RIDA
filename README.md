# RIDA - Remote Intrusion Detection Analyzer

## What is RIDA?

RIDA is an intrusion detection system designed to monitor a specific folder within a system, ensuring that attributes such as file size, permissions, and inode information remain unchanged.

Existing examples of intrusion detection systems include [AIDE](https://aide.github.io/) and [Linux IMA](https://linux-ima.sourceforge.net/).

## Why RIDA?

While AIDE and IMA serve their purpose, they come with significant limitations that restrict their usability across a broad spectrum of systems requiring integrity. RIDA addresses these limitations by introducing four key features:

- **Remote Control:** RIDA allows remote control of the integrity process, enabling adjustments to integrity parameters based on changing requirements. AIDE and IMA lack this remote control functionality.
- **Smart Embedded Check System:** Unlike AIDE and IMA, RIDA incorporates a smart embedded check system. This feature ensures that users do not have to devise their own system checks, enhancing user-friendliness.
- **Built-in Actions on Integrity Violation:** RIDA includes built-in actions in case of integrity violations. This proactive approach sets RIDA apart from its counterparts.
- **Distributed Knowledge Base:** In the era of large-scale networks and data centers, RIDA facilitates the automatic distribution of integrity rules across multiple computers. This functionality is not present in AIDE and IMA.

## How

RIDA is conceptualized as a distributed system with a master node coordinating a group of computers. While a P2P network adds almost no value, the use of Distributed Ledger Technology is preferred but it must be studied to understand if a DLT is the best fit for the target.

The development of RIDA involves collaboration across multiple disciplines:

- **Network Security:** Ensuring secure connections between peers.
- **Distributed Systems Knowledge:** Developing a robust algorithm for propagating integrity rules among systems within the same network.
- **System Development:** Primarily targeting Linux systems.
- **Web Development:** Implementing a user-friendly UI to interact with the main node.
- **Blockchain Knowledge:** Desired for enhancing the system's capabilities.

## Cloud Native Approach

When envisioning this tool, a crucial aspect is its cloud-native readiness, ensuring seamless integration with major cloud products such as Kubernetes and its derivatives. The preliminary concept involves a Kubernetes controller with the capability to scan running containers, identifying and addressing integrity issues.

The idea is still in its early stages, and while contemplating its usefulness, I acknowledge the current lack of visibility into Kubernetes/container vulnerabilities. As my understanding of this topic evolves, I will promptly update this document to provide more insights.