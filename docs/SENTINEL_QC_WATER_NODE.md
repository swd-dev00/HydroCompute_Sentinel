# Sentinel QC Water Node Simulator

The Sentinel QC Water Node Simulator is a telemetry integrity demonstration layer that simulates water sensor data for HydroCompute infrastructure readiness evaluation.

## Purpose
- Show how field data (temperature, discharge, device health, connectivity) can support situational awareness for infrastructure siting decisions.
- Provide two decision-support scores:
    - QC Confidence Score (sensor-level reading quality)
    - Field Telemetry Integrity Score (overall monitoring system readiness)

## How It Works
- Synthesizes example sensor and telemetry quality metrics (health, calibration, reliability, etc.)
- Returns numerical and classified scores:
    - Trusted / Usable with caution / Human review required / Reject
    - Field Ready / Deployable with monitoring / Pilot only / Not reliable
- Intended for reproducible demo; not used for real-time operational safety.

## Related source files
- `telemetry_scoring.py`
- `run_demo.py`

## Limitations
- Demo only: no live field sensors, control systems, or regulatory data integration.
- Real-world configuration requires robust QA/QC, failover, and cybersecurity beyond this layer.
