MujinMI API Overview

The MujinMI (Machine Intelligence) API is the primary gateway for developers to interact with the MujinOS environment. It allows for high-level motion planning, real-time perception queries, and robot state management.

🔑 Authentication

All API requests must be authenticated. When using the Python SDK, provide your API key during controller initialization.

Header: X-Mujin-API-Key

Scope: Ensure your key has Write permissions for motion commands.

🚀 Quick Start: Python SDK

The easiest way to get started is by using our native Python wrapper. It abstracts the underlying REST/gRPC calls into simple method signatures.

import mujin_sdk

# Initialize the controller
controller = mujin_sdk.Controller(
    ip="192.168.1.100", 
    api_key="your_secret_key"
)

# Access a specific robotic arm
robot = controller.get_robot("primary_arm")


🛠 Python SDK Reference (Auto-generated)

The following section is synchronized directly with our src/ directory.

RobotController Class

::: src.mujin_interface.RobotController

💡 Best Practices

Error Handling: Always wrap motion commands in a try-except block.

Safety First: Commands are subject to hardware safety limits.