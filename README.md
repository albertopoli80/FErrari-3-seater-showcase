## 📺 Demonstration & Media

### Phase 1: Laboratory Bench Integration & ECU Simulation
Before vehicle installation, the entire Formula 1 electrical ecosystem was simulated on a workbench. An Arduino board was programmed to forge CAN-bus packets, recreating dynamic engine loads, RPM sweeps, and rapid gear shifts (up to 280+ km/h) to stress-test the rendering latency of the HMI software.

<video src="tre.mp4" width="100%" controls></video>

### Phase 2: Final Vehicle Integration (Ferrari F1 3-Seater)
The finalized HMI dashboard mounted directly into the red carbon-fiber cockpit structure of the F1 Three-Seater. The software successfully processed synchronized acoustic and visual telemetry lines directly inside the live monocoque environment.

<video src="f3seater.mp4" width="100%" controls></video>

# High-Performance Automotive HMI & Edge Telemetry Prototype
## R&D Project | Formula 1 Three-Seater Custom Dashboard (2012 - 2014)

A pioneering edge-computing telemetry and Human-Machine Interface (HMI) system developed for the legendary **Ferrari F1 Three-Seater** chassis. Designed and engineered under tight constraints to bridge hardware layer limitations with low-latency software performance in an extreme vibration and high-frequency environment.

---

## 🏎️ Executive Summary & Core Challenges

The goal was to design, test, and integrate a custom passenger-facing dashboard into a modified Formula 1 three-seater monocoque. The system had to process real-time vehicle telemetry directly from the engine control unit (ECU) via the CAN bus, handling complex graphics and dynamic data reproduction under brutal physical conditions.

### The Physics Enemy: High-Frequency Vibrations
In motorsport engineering, software reliability is deeply coupled with physical constraints. The chassis vibrations (reaching frequencies up to 800 Hz) constantly threatened the structural integrity of commercial-grade connetions. Micro-disconnects at the hardware layer cause volatile kernel-level file descriptor drops (USB attach/detach cycles). The software architecture had to be aggressively resilient to survive these hardware dropouts.

---

## 🛠️ Architecture & Data Pipeline

To achieve maximum determinism and avoid memory allocation overhead, the system bypassed high-level abstractions in favor of a lean, "close-to-the-metal" pipeline.
