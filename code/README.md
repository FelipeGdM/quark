# Code

```mermaid
flowchart TD
    agent_teleop(quark_agent_teleop) --> perception(quark_perception)
    agent_teleop --> control(quark_control)
    perception --> camera(quark_camera_bringup)
    control --> motor(quark_motor_bringup)
    subgraph quark_driver
        motor(quark_motor_bringup)
        camera(quark_camera_bringup)
    end
```
