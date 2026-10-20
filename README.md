# HRS · Humanoid Robotics Team Project

ROS 2 components for visual target selection, humanoid task sequences and shared robot-control interfaces.

## Code map

- `src/vision/vision/vision/`: ArUco detection, color/shape processing, undistortion and target selection.
- `src/vision/vision/launch/detector.launch.py`: combined vision-pipeline entry.
- `src/teleop/`: task coordination, marker-guided approach and manipulation sequences.
- `src/ainex/`: robot descriptions, controller and servo interfaces, including vendor-derived components.
- `src/llm/`: shared speech/LLM interfaces, messages and bringup packages.

## Local run

In a configured ROS 2 workspace with the required interfaces available:

```bash
colcon build --symlink-install
source install/setup.bash
ros2 launch vision detector.launch.py
```

Hardware/vendor assets, camera configuration, credentials and local endpoints are not included; configure them locally before running.

This is team coursework with student, instructor and vendor components; existing attribution and Apache/BSD notices remain, and no new blanket license is applied. See `EXCLUDED.md`.
