# MujinMI API Overview

MujinMI (Machine Intelligence) provides a RESTful API and a Python SDK to control motion planning.

### Authentication
All requests must include an `X-Mujin-API-Key` in the header.

### Sample Request: Get Joint States
```python
import mujin_sdk

controller = mujin_sdk.Controller(ip="192.168.1.100")
robot = controller.get_robot("primary_arm")

# Retrieve real-time joint positions
print(robot.get_joint_states())