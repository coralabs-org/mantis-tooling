# MANTIS Tooling

## Overview
MANTIS is an AI maintenance copilot built for factory engineers and technicians. It consolidates technical manuals, historical maintenance reports, and real-time sensor streams so crews can sidestep delays caused by scattered or stale documentation. By learning from past incidents across machines and sites, MANTIS continuously sharpens troubleshooting accuracy while preserving critical organizational knowledge. Its acoustic and visual diagnostics run on standard smartphones—no dedicated hardware required—keeping frontline teams agile on the plant floor.

### What Exists Today
- **Acoustic diagnostic model:** Technicians capture short machine audio clips with a phone. MANTIS processes each recording with spectral and Gabor transforms to surface anomalies and classify likely mechanical issues, shortening the path from symptom to root cause.

## Sensor-Based Tools Ideation
This repository gathers, evaluates, and iterates on new smartphone-sensor-powered diagnostic concepts that could slot into MANTIS. We welcome ideas from reliability engineers, controls specialists, ML researchers, and practitioners everywhere.

**Focus on sensors already available on mainstream smartphones:**
- Microphone
- Camera
- Accelerometer
- Gyroscope
- Magnetometer
- Proximity sensor
- Light sensor

### Inspiration Concepts
- Visual vibration analysis via optical flow
- Thermal pattern estimation from RGB video (no thermal camera required)
- Accelerometer-based vibration spectrum health check
- Magnetic field irregularity detection for motors or transformers
- Conveyor belt speed tracking with computer vision
- Idle sound deviation detector
- QR/NFC-triggered contextual maintenance workflows
- Visual wear detection on belts, bearings, or couplings

## How to Share an Idea
Open an issue or pull request and include:
- **Tool name**
- **Sensors used**
- **Problem**
- **High-level approach**
- **Benefits**
- **Limitations**

Check the [idea proposal template](.github/ISSUE_TEMPLATE/sensor-tool-idea.md) for a ready-to-copy format.

## Community
Contributions of all sizes are welcome. Share sketches, link prior art, or prototype quick experiments—anything that helps move phone-native diagnostics forward for frontline maintenance teams. Let’s build the next wave of smart tools together.

