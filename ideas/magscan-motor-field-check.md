# MagScan – Motor & Transformer Magnetic Field Check (Smartphone)

## Tool name
MagScan: Guided magnetic signature scan for rotating equipment and transformers.

## Sensors used
- Magnetometer (primary)
- Gyroscope + accelerometer (for motion/position tracking and scan stability)
- Optional: microphone (correlate with electrical hum / mechanical noise)

## Problem
Electrical issues (phase imbalance, loose connections), rotor/stator defects, and transformer problems can create abnormal magnetic fields. On the shop floor, technicians often lack quick screening tools and must wait for specialized instruments.

## High-level approach
1) **Guided scan**: The app guides the user to slowly move the phone around key points:
   - Motor drive end / non-drive end
   - Around the stator housing (4 quadrants)
   - Near terminal box / cable entry
   - For transformers: around core/coil regions and bushings (safe distance)
2) **Stabilize & track**: Use gyro/accel to detect consistent sweep speed and reject shaky segments.
3) **Feature extraction** (from magnetometer time series):
   - RMS magnitude and variability
   - Spectral peaks and harmonic structure
   - Symmetry checks across quadrants
   - “Hotspot” detection: localized spikes during scan
4) **Reference & comparison**:
   - Compare against a baseline scan for the same asset (if available)
   - Otherwise compare against a library of “healthy” ranges by motor size/type
5) **Output**:
   - Simple score: OK / Monitor / Investigate
   - “Likely causes” hints (e.g., loose terminal connection, imbalance, broken rotor bar suspicion)
   - A saved scan report (time, asset ID, environment notes)

## Benefits
- Quick screening using only a phone (no specialized gear)
- Helps prioritize which assets need deeper inspection
- Builds a historical baseline per asset to catch drift early

## Limitations / risks
- Magnetometer readings are sensitive to nearby steel, tools, and phone orientation
- Needs safe operating procedure (distance from high-voltage, rotating parts)
- Best results when a baseline “healthy” scan exists for the same machine

## Validation plan
- Collect scans from known-good assets vs assets with documented faults
- Cross-check with traditional measurements (vibration, current signature analysis where available)
- Evaluate false positives in high-metal environments; add UI prompts for mitigation
