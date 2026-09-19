# Argus — Wearable Visual–Inertial Odometry

A wearable sensing prototype that combines camera and inertial measurements for motion estimation, with a host-side workflow for human-motion visualization.

**Area:** Robot perception  
**Stage:** Research prototype; source repository private  
**Tools and methods:** C++17 · ROS 2 · OpenCV · Eigen · Raspberry Pi · OpenSim

## Hardware gallery

| Sensor module and mounting plate | Camera and IMU electronics |
| --- | --- |
| ![Physical sensor module](../../media/argus/sensor-module.jpg) | ![Camera and IMU electronics](../../media/argus/camera-imu-electronics.jpg) |

*Original hardware photographs from a historical project report. These show the sensing assembly; they are not a benchmark or a claim about the current software version. [Media sources](../../docs/MEDIA.md).*

## Context

Research at the Stanford Assistive Robotics and Manipulation Lab.

## My contribution

- Developed a Raspberry Pi-based sensing prototype and worked on camera–IMU calibration, synchronization, and system integration.
- Implemented and tuned a lightweight ROS 2 visual–inertial odometry pipeline.
- Integrated sensor streams with OpenSim for motion reconstruction and kinematic visualization.

## Technical approach

The documented VIO implementation uses KLT feature tracking, IMU propagation, and a multi-state constraint Kalman filter. It publishes odometry and covariance estimates through ROS 2.

## Available materials and validation

An existing code repository and local implementation are available. Benchmark datasets and reproducible evaluation results are not included in this portfolio. The documented estimator requires stationary initialization and does not include loop closure.

[Source repository — private; access required](https://github.com/YuhaoHuai/Argus)

[Back to all projects](../README.md) · [Portfolio home](../../README.md)

