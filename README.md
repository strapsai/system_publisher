Content created by Yaoyu's AI assistant. Use with care.

# System Publisher

`system_publisher` is a ROS 2 Python package used for publishing system-level metrics and hardware status. It is designed to provide high-level situational awareness of a robot's onboard computer health, including CPU usage, memory availability, and network statistics.

## Overview

The package features a monitoring node that periodically samples system resources and publishes them as ROS 2 messages. This allows operators to identify performance bottlenecks or potential system overloads during intensive missions like the DARPA Triage Challenge (DTC).

## Key Features

- **Resource Monitoring**: Tracks CPU load (per-core and average), memory usage, and disk space.
- **Network Statistics**: Monitors interface-level data rates to identify bandwidth constraints.
- **Hardware Telemetry**: Optionally includes thermal and power metrics if supported by the host hardware.
- **Cross-Platform**: Designed to run on common robotic compute platforms like NVIDIA Jetson/Orin and standard x86 laptops.

## Repository Structure

- `system_publisher/main.py`: Main entry point for the resource monitoring node.
- `system_publisher/subscriber.py`: Utility for verifying published system metrics.

## Prerequisites

- **ROS 2 Humble**
- **Python 3.10+**
- **psutil**: Python library for system monitoring.
- **Dependencies**:
  - `rclpy`
  - `std_msgs`

## Installation

1. Clone the repository into your ROS 2 workspace:
   ```bash
   cd ~/ros2_ws/src
   git clone https://github.com/strapsai/system_publisher.git
   ```

2. Build the package:
   ```bash
   cd ~/ros2_ws
   colcon build --packages-select system_publisher
   ```

## Usage

Launch the system publisher:
```bash
ros2 run system_publisher main
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
