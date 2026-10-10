# Edge-Cloud Adaptive Quantization & Resolution Broker

A lightweight Python simulation modeling an intelligent edge gateway broker that dynamically optimizes task distribution, precision tiers, and stream resolution to meet strict Service Level Agreements (SLAs) under fluctuating network conditions.

---
MARYAM FAGBO
---

## Overview

In advanced distributed edge intelligence systems, streaming uncompressed high-resolution data to the cloud introduces severe bandwidth bottlenecks, while running deep models locally on resource-constrained hardware triggers thermal throttling. This project implements:
1. **Real-Time Telemetry Tracking:** Monitors stochastic wireless throughput and cloud server queue latencies.
2. **Utility-Maximization Policy Broker:** Automatically determines whether to execute quantized INT8 inference locally, scale input resolution dynamically, or offload heavy FP32 payloads to remote cloud infrastructure.
3. **Multi-Variable Analytics:** Generates multi-panel telemetry plots mapping congestion against active QoS execution tiers and resultant inference accuracy.

---
## Results & Visualization

When executed, the simulation outputs quantitative metrics and renders a three-panel performance diagram tracking:


1. **Top Panel:** Network throughput and server queue latency fluctuations.
2. **Middle Panel:** Active QoS execution tier timeline.
3. **Bottom Panel:**  Resulting operational accuracy across request sequences.

---
## How to Run 

You can view and execute this notebook directly in Google Colab:
https://colab.research.google.com/drive/1TLAppcVugOgWUm_cNRp_0XvQo9sm6Gsa?usp=sharing
---

## Code Architecture

* **Dependencies:** `numpy`, `matplotlib`
* **Core Paradigm:** Threshold-based dynamic control system and service-level optimization across edge-cloud boundaries.
* **Execution Environment:** Designed for rapid validation in Google Colab or standard Python environments.

```python
# Core broker decision policy snippet
if bw < 5.0 or lat > 80.0:
    mode = 0  # Local INT8 Quantized Execution
elif 5.0 <= bw < 20.0:
    mode = 1  # Resolution-Scaled Offload
else:
    mode = 2  # Remote Heavy Cloud (FP32)
