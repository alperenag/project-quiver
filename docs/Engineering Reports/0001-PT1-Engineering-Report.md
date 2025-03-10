# **Project Quiver PT1 Engineering Report**

Chapter assignment: https://docs.google.com/spreadsheets/d/1HtNkbYEaUmdiHmNGzjgIHoH00VwN5BeEsrYEDDL5YV4/edit?gid=0#gid=0
Spearhead Engineering Report: https://docs.google.com/document/d/11yaRfGD6EVfLsOcSKlHVtQumxKxEsTgK/edit

---

# 1. **Introduction**

The purpose of Project Quiver is to design and manufacture a practical multi-purpose multi-rotor unmanned aerial vehicle. Its purpose is to promote Arrow's decentralized organization to explore the commercial aviation service market and generate new concepts for the manufacturing process of subsequent unmanned and manned aircraft models. And try to break the current lack of innovation in the drone market around the United States and even the world by Internet collaborate and Internet finance.   

This aircraft is designed to perform typical light UAV missions. The design concept is: compact and portable, easy to manufacture, easy to maintain, highly reliable, highly adaptable, and expandable.

The PT1 prototype of this Project Quiver will contain the following features:
- Having a common quadcopter layout to ensure energy efficiency and structure simplified.
- The designated maximum mission load is 25 kg. Considering the safety margin, the designated maximum thrust force is about 45 to 50 kg.
- The motor beams and can be folded to the side for optimized storage and transportation.
- Standardized, quick-detachable mission attachment interface.
- Has the functions supported by the digital autopilot system, such as GNSS-assisted hovering, waypoint missions, radar altimeter, etc.
- Has FPV camera and video transmission to assist piloting and various mission actions.
- Use 14-cells LiHV smart batteries and advanced main power connectors commonly used by heavy drones.
- Partially use CAN bus for communication to avoid electromagnetic interference that traditional non-differential signals such as PWM may be subject to.
- Has digitalized sensor communication to monitor more component parameters, such as battery cell temperature and ESC temperature.
- Using integrated thrust terminal to improve the reliability and design convenience of the thrust system, and for easier sourcing, installing and initial testing.
- Use large PDB and circuit breakers previous designed for Project Feather to improve the safety and controllability of the power distributing system.

Based on the above characteristics, Project Quiver will also try to compete with other UAVs on the market in terms of parameters such as endurance, empty weight ratio, open source level, and mission equipment options. It's also planned to gradually introduce more advanced designs including but not limited to the following in future prototypes:
- RTK high-precision GNSS positioning
- Dedicated PDB
- Dedicated battery pack
- Dedicated thrust system ESC
- Integrated 3D printing structure
- Hazard protection airframe
- Multiple mission attachment interface
- Retractable landing gear
- Emergency ballistic parachute
- ...

The initial version doesn't have a waterproof and dustproof design, and the only equipment hanging point of the fuselage was located on the belly of the airframe for easier configuration operations. The first experimental commercial project is the herbicide dispenser "Brush Bullet Pod" and its corresponding vegetation analysis and in-flight dispensing services.

The design process of Project Quiver mainly uses Onshape and Fusion 360 for CAD/CAM software. Since the project doesn't specify the use of specific industrial design software, the STEP and other formats will be used as data exchange formats when working between multiple software.

<!-- Chinese origin 中文原文（未纠错和润色）

Project Quiver的目的是设计并制造一款实用性多用途多旋翼无人飞行器，其目的是为了推动Arrow去中心化组织探索商业航空服务市场、为后续无人和载人飞行器型号的制造流程产生新的概念。并尝试使用互联网协作和互联网金融，打破现今美国乃至全世界无人机市场缺乏创新的局面。  
  
本飞行器设计为执行典型的轻型无人机任务，设计理念是：紧凑便携、易制造、易维护、高可靠、高适应、可拓展。  
  
此工程的PT1原型机将具有以下特点：  
- 采用常见的四旋翼布局，以确保能源效率和结构简易。
- 设计最大任务载荷为25公斤，考虑到安全裕度，设计最大拉力约为45至50公斤。
- 机臂、螺旋桨桨叶可向侧面折叠，以优化收纳和运输。
- 标准化、可快拆式的任务载荷挂架。
- 具备GNSS辅助悬停、航点任务、雷达高度计等数字化自动驾驶仪所支持的功能。
- 具备FPV相机和视频传输，以辅助飞行驾驶和各类任务动作。
- 采用大型无人机普遍使用的14串LiHV智能电池和先进的主电源连接器。
- 部分系统使用CAN总线进行通讯，避免PWM等传统非差分信号可能受到的电磁干扰。
- 采用数字化通讯的传感器以监视更多部件参数，例如电芯温度、ESC温度。
- 采用集成一体化动力终端，提升动力系统可靠性和设计便捷性，同时易于采购安装和初期测试。
- 采用先前为Project Feather设计的大型PDB和断路器，以提升配电系统的安全性和可控性。

基于以上特性，Project Quiver还将尝试在续航性能、空重比、开源程度、任务载荷选项等参数上与市面其他无人飞行器相角逐。并计划在未来的原型机型逐步引入包括但不限于以下内容的更先进的设计：  
- RTK高精度GNSS定位
- 专用PDB
- 专用电池组
- 专用动力系统ESC
- 一体化3d打印结构
- 危害防护型机身
- 多载荷挂架
- 可收放起落架
- 紧急弹道降落伞
- ...

初期版本并未采用防水防尘设计，且机体的唯一一个装备挂点位于机身腹部，以方便调测。目前首个实验性商业项目为除草剂投放器“Brush Bullet Pod”与其对应的植被分析、空中撒放服务。      
  
Project Quiver的设计流程主要使用的软件为Onshape和Fusion 360，由于项目未规定采用特定的工业设计软件，所以在多个软件间工作时，将使用STEP等格式作为数据交换格式。

End Chinese origin -->

# 2. PROJECT REQUIREMENTS 

### 2.1 Flight-Critical Systems

Project Quiver PT1 must incorporate robust and reliable flight-critical systems to ensure safe and predictable flight performance. The UAV shall feature advanced flight-control electronics that maintain stable operation under varying flight conditions and payload configurations. These systems will prioritize redundancy, allowing the drone to safely land even if certain critical components fail during flight operations.

### 2.2 Structural Integrity and Components

The structural frame shall leverage commercially available, off-the-shelf components to enable rapid assembly and ease of replacement. The chosen materials must be lightweight yet strong enough to sustain heavy lift operations, accommodating considerable payload capacities without compromising durability or structural safety. Additionally, the structural configuration must allow flexibility for future iterations.

### 2.3 Electrical Systems and Power Management

A simplified and robust electrical system shall be designed, ensuring reliability and ease of troubleshooting. Commercially available battery packs must support adequate flight durations, providing sufficient power for continuous flight under maximum payload conditions. The power system should include protective features such as circuit breakers or fuses, mitigating the risk of electrical overload or failures.

### 2.4 Payload Integration and Imaging

The UAV prototype shall integrate a stabilized camera system mounted on a gimbal, providing steady, high-quality video feeds to ground operators. An adaptable payload attachment mechanism must enable rapid payload swaps in-field, thus maximizing versatility across various mission profiles.

### 2.5 Flight Testing and Verification

A comprehensive testing program is required for PT1, verifying core flight performance, structural strength, electrical reliability, and payload handling capabilities. Testing should document essential parameters and establish baseline operational limits, providing valuable data to inform subsequent design iterations.

----------

# 3. PROTOTYPE SPECIFICATIONS

### 3.1 Flight-Critical Systems

-   **Flight Controller**: Utilize Pixhawk or an equivalent open source controller capable of advanced flight management, precision navigation, and autonomous flight modes. Must include redundancy across critical sensors (IMU, GPS, barometer).
-   **Navigation Sensors**: Include dual GNSS modules, providing high accuracy positioning with Real-Time Kinematics (RTK) support to facilitate precise waypoint navigation and payload delivery.

### 3.2 Structure and Geometry

-   **Frame Material**: Employ carbon fiber tubes interconnected with aluminum joints for strength-to-weight optimization. The frame configuration shall accommodate interchangeable arm sections to simplify repairs and upgrades.
-   **Maximum Takeoff Weight (MTOW)**: Prototype must support a total weight exceeding 25 kg.
-   **Payload Capacity**: Minimum payload capability of 10 kg is required to validate heavy-lift capabilities.
-   **Structural Safety Factor**: Structural integrity must ensure a safety factor of at least 2.5 times the maximum anticipated operational loads.

### 3.3 Propulsion and Power

-   **Motors and ESCs**: Select commercial-grade brushless DC motors rated for 12S to 14S battery configurations, paired with ESCs capable of sustaining at least 80A continuous current, ensuring sufficient thrust-to-weight performance.
-   **Battery System**: LiPo or Li-Ion battery packs rated at 12S or 14S voltage levels must guarantee a minimum of 20 minutes endurance under fully loaded conditions.
-   **Propellers**: Integrate foldable carbon-fiber propellers optimized specifically for heavy-lift efficiency, minimizing noise and maximizing flight endurance.

### 3.4 Electrical Systems

-   **Electrical Layout**: Wiring harnesses shall be modular and clearly labeled for ease of maintenance and fault isolation. All wiring must be heat-resistant and abrasion-resistant to withstand harsh operational environments.
-   **Power Distribution**: Install dedicated circuit breakers or resettable fuses to protect critical flight electronics and payload circuits from potential short circuits or electrical surges.

### 3.5 Payload Handling and Camera

-   **Gimbal System**: Implement a 3-axis stabilized gimbal, providing precise control of camera orientation to deliver steady footage even in turbulent flight conditions.
-   **Camera Capabilities**: Equip PT1 with a camera capable of delivering at least 1080p resolution at 30fps, streaming live footage directly to the ground control system with minimal latency.
-   **Payload Attachment Interface**: Establish a quick-release payload rail system with adjustable balance points, enabling secure payload attachment and easy in-field interchangeability.

### 3.6 Flight Control and Telemetry

-   **Communication Systems**: Employ telemetry links capable of maintaining reliable communication over distances of at least 2 km, utilizing 900 MHz or 2.4 GHz bands, backed by a redundant 433 MHz communication link as a fallback option.
-   **Ground Control Station (GCS)**: Real-time telemetry data, including flight parameters, payload conditions, and battery health, must be continuously transmitted to the operator’s interface.

### 3.7 Environmental and Operational Specifications

-   **Operating Temperature**: The drone shall reliably operate in a temperature range from -10°C to +45°C, enabling effective use in diverse environmental conditions.
-   **Wind and Moisture Resistance**: Prototype must maintain stable flight control in wind speeds up to 25 km/h and include basic splash-resistant protection for electrical and propulsion systems, protecting against incidental moisture exposure.

### 3.8 Maintenance, Assembly, and Documentation

-   **Assembly Instructions**: BOMs and detailed assembly instructions should be created and provided.
-  **Assembly Efficiency**: Assembly of the UAV, including installation of payloads and batteries, shall be achievable within 60 minutes by trained personnel from packaged state.
-   **Maintenance Schedule**: A clear and concise maintenance manual detailing procedures and inspection intervals must be provided.

### 3.9 Flight Testing and Validation

-   **Initial Flight Tests**: Conduct controlled test flights covering hover stability, maneuverability, payload management, and endurance under realistic operational scenarios. All results and incidents should be carefully documented.
-   **Documentation**: Provide comprehensive documentation, including flight logs, inspection reports, photographic and video evidence of successful testing outcomes, ensuring traceability of performance improvements for future iterations.

# 4. **Mission Performance**

Hey guys how are you doing

# 5. **Flight Mechanics**

Hey guys how are you doing

# 6. **Propulsion System**

Hey guys how are you doing

# 7. **Electrical System**

Hey guys how are you doing

# 8. **Geometry & Structure**

Hey guys how are you doing

# 9. **Appendix**

Hey guys how are you doing

