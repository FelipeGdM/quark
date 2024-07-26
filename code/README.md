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
        motor --> vesc(vesc_driver)
        camera --> depth_ai(depthai_ros_driver)
    end

    classDef extDep fill:#f9f;

    class vesc,depth_ai extDep;
```
