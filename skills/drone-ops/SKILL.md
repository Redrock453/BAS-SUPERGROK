---
name: drone-ops
description: Context for grim-fpv-ai autonomous FPV drone project on Jetson Orin NX.
---

# Drone Ops Skill

## Stack
- OpenVINS (SLAM/VIO)
- YOLOv8 + ByteTrack
- WorldModel (state aggregator)
- HFSM + NAVIGATION
- Jetson Orin NX

## Repo
github.com/Redrock453/grim-fpv-ai

## Key modules
- data_contracts.py
- state_machine.py
- event_bus.py
- world_model.py
- sensor_sync.py
- openvins_bridge.py
- detector.py
- tracker.py

## Run
```bash
cd ~/grim-fpv-ai
python3 main.py
```
