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

# 2. Project Requirements

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

# 3. Prototype Specifications

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

Below is a mission performance analysis of maximum possible flight time for two missions: Surveillance and Waypoint Missions both under a Tattu 3.5 14S LiHV 30 Ah battery.

Key assumptions:

- **Usable Battery**: 21.6 Ah (after 2C derating to ~27 Ah, then a 20% reserve).  
- **Propulsion**: 4 Hobbywing X6 Plus motors.  
- **Mission Legs**: short, fixed‐time take‐off, climb, descent, landing; the remaining time is the main mission leg.
- **Real-World Effects**: Climb rates, aerodynamic efficiency, battery health, and environmental conditions do not affect the performance..  

## 4.1. Surveillance Mission

In this mission, the aircraft hovers with 20 kg MTOW without any payload, using its camera for surveillance.

### 4.1.1. Current Requirements

- Hover Current (20 kg): ~40.9 A (estimated from thrust‐vs‐current data of Hobbywing X6 Plus).  
- Take‐Off / Climb (110%): ~48.6 A  
- Descent (90%): ~35.5 A  
- Landing (100%): ~40.9 A

### 4.1.2. Mission Leg Times

- Take‐off: 0.5 min  
- Climb: 1.5 min  
- Descent: 1.0 min  
- Landing: 1.0 min  

Convert each to hours and multiply by current to get amp‐hours.

1. **Take‐off (0.5 min)**  
   - 0.5 min = 0.0083 hr  
   - 48.6 A × 0.0083 hr ≈ 0.40 Ah  

2. **Climb (1.5 min)**  
   - 1.5 min = 0.025 hr  
   - 48.6 A × 0.025 hr = 1.22 Ah  

3. **Descent (1.0 min)**  
   - 1.0 min = 0.0167 hr  
   - 35.5 A × 0.0167 hr ≈ 0.59 Ah  

4. **Landing (1.0 min)**  
   - 1.0 min = 0.0167 hr  
   - 40.9 A × 0.0167 hr ≈ 0.68 Ah  

Sum of non‐mission legs = **2.89 Ah**.

### 4.1.3. Maximum Hover Duration

Remaining capacity for hover = 21.6 Ah − 2.89 Ah = **18.71 Ah**.  
At 40.9 A (hover), available hover time = 18.71 Ah ÷ 40.9 A ≈ **0.457 hr** = ~27.4 min.

**Total Surveillance Flight Time**  
- Non‐mission legs: 0.5 + 1.5 + 1.0 + 1.0 = 4.0 min  
- Hover: ~27.4 min  
- **Overall**: ~31.4 min  

## 4.2. Waypoint Mission

In this mission, the aircraft travels with 25 kg MTOW between waypoints. The power consumption for forward flight is assumed as 120% of hover.

### 4.2.1. Current Requirements

- Hover Current (25 kg): ~57.5 A  
- Forward Flight (120%): ~69 A
- Take‐Off/Climb (110%): ~66.5 A  
- Descent (90%): ~49.9 A  
- Landing (100%): ~57.5 A

### 4.2.2. Mission Leg Times

- Take‐off: 1.0 min  
- Climb: 2.0 min  
- Descent: 1.0 min  
- Landing: 1.0 min  

1. **Take‐off (1.0 min)**  
   - 1.0 min = 0.0167 hr  
   - 66.5 A × 0.0167 hr ≈ 1.11 Ah  

2. **Climb (2.0 min)**  
   - 2.0 min = 0.0333 hr  
   - 66.5 A × 0.0333 hr ≈ 2.22 Ah  

3. **Descent (1.0 min)**  
   - 1.0 min = 0.0167 hr  
   - 49.9 A × 0.0167 hr ≈ 0.83 Ah  

4. **Landing (1.0 min)**  
   - 1.0 min = 0.0167 hr  
   - 57.5 A × 0.0167 hr ≈ 0.96 Ah  

Sum of these legs = **5.12 Ah**.

### 4.2.3. Maximum Forward‐Flight Duration

Remaining capacity for forward flight = 21.6 Ah − 5.12 Ah = **16.48 Ah**.  
At 69 A, flight time = 16.48 Ah ÷ 69 A ≈ **0.239 hr** = ~14.3 min.

**Total Loiter Flight Time**  
- Non‐mission legs: 1.0 + 2.0 + 1.0 + 1.0 = 5.0 min  
- Forward flight: ~14.3 min  
- **Overall**: ~19.3 min  

# 5. **Flight Mechanics**

Hey guys how are you doing

# 6. **Propulsion System**

Based on the QUIVER project specifications, alternative manufacturers for electric motors, compatible propellers, and ESCs were evaluated.

## Table X. Drone Propulsion System Comparison for 25 kg MTOW

| Feature                         | System 1                       | System 2                       | System 3                       | System 4                       | System 5                       | System 6                                     |
| ------------------------------- | ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ | -------------------------------------------- |
| **Motor**                       | MAD 6215 IPE                   | T-Motor P80Ⅲ P                 | T-Motor P60                    | MAD M6C12 EEE                  | Freerchobby FRC Heavy          | Hobbywing XRotor X6 Plus (integrated system) |
| **Max Thrust**                  | 11.5 kg                        | 16 kg                          | 8.5 kg                         | 9.4 kg                         | 11.5 kg                        | 11.822 kg                                    |
| **Voltage (V)**                 | 44.4V (12S)                    | 44.4V (12-14S)                 | 44.4V (12-14S)                 | 44.4V (12-14S)                 | 48V (6S-12S)                   | 44.4V (12-14S)                               |
| **Max Current (A)**             | 60A                            | 70A                            | 38A                            | 36.2A                          | 59.7A                          | 51.8A                                        |
| **Price (USD)**                 | $98                            | $199.9                         | $107.9                         | $129                           | $62                            | $97                                          |
| **Weight (g)**                  | 370 g                          | 649 g                          | 225 g                          | 257 g                          | 370 g                          | 710 g (integrated)                           |
| **Recommended Propeller**       | 21-22"                         | 30-32"                         | 22"                            | 21-24"                         | 22"                            | 24"                                          |
| **Propeller Cost Estimation**   | $28                            | $45                            | $28                            | $28                            | $28                            | Included                                     |
| **Propeller Weight Estimation** | 0.065 kg                       | 0.170 kg                       | 0.065 kg                       | 0.065 kg                       | 0.065 kg                       | Included                                     |
| **ESC**                         | MAD AMPX 80A (5-14S) Drone ESC | MAD AMPX 80A (5-14S) Drone ESC | MAD AMPX 80A (5-14S) Drone ESC | MAD AMPX 80A (5-14S) Drone ESC | MAD AMPX 80A (5-14S) Drone ESC | Included                                     |
| **ESC Cost**                    | $60                            | $60                            | $60                            | $60                            | $60                            | Included                                     |
| **ESC Weight**                  | 0.19 kg                        | 0.19 kg                        | 0.19 kg                        | 0.19 kg                        | 0.19 kg                        | Included                                     |
| **System Thrust**               | 46 kg                          | 64 kg                          | 34 kg                          | 37.6 kg                        | 46 kg                          | 47.288 kg                                    |
| **System Weight**               | 2.5 kg                         | 4.035 kg                       | 1.92 kg                        | 2.048 kg                       | 2.5 kg                         | 2.84 kg                                      |
| **System Cost**                 | $744                           | $1,219.6                       | $783.6                         | $868                           | $600                           | $388                                         |

The **Hobbywing XRotor X6 Plus integrated propulsion system** is selected as the best match for QUIVER propulsion requirements in terms of thrust, weight, and cost. Integrated propulsion systems combine a motor, ESC, and propeller into one optimized unit. This system offers the lowest cost compared to other evaluated options, with comparable weight. It includes power cables which can be trimmed to the necessary length. Advantages of an integrated system include optimized performance due to matched components, reduced electrical losses from shorter wiring, improved aerodynamics, and waterproof casing, significantly reducing installation workload.

## Selected Battery

The **Tattu 14S HV 30000mAh Smart Battery** is chosen for its integrated battery management system (BMS) and efficient mechanical integration. The battery connects to the drone through a specialized Molex connector, secured by a safety latch.

| Specification                        | Details                                     |
| ------------------------------------ | ------------------------------------------- |
| **Configuration**                    | 14S1P (14 series, 1 parallel)               |
| **Nominal Capacity**                 | 30,000 mAh (0.2C, 4.3-3.0V)                 |
| **Minimum Shipping Voltage**         | 52.5 \~ 54.6V (3.75-3.9V per cell)          |
| **Nominal Voltage**                  | 53.2V (3.8V per cell)                       |
| **Internal Resistance**              | 9 ± 3.5 mΩ (1 kHz AC method)                |
| **Dimensions (H×W×L)**               | MOLEX: 103 × 251 × 333 mm                   |
| **Battery Weight**                   | 11,200 ± 300 g                              |
| **Charging Mode**                    | CC-CV (Constant Current – Constant Voltage) |
| **Maximum Charging Voltage**         | 60.9V                                       |
| **Standard Charging Current**        | 6A (0.2C, \~450 min charge time)            |
| **Fast Charging Current**            | 150A (5C, \~18 min charge time)             |
| **Discharge Cut-off Voltage**        | 3.0V/cell @ 0.2C, 3.3V/cell @ ≥0.5C         |
| **Standard Discharge Current**       | 6A (0.2C, \~270 min discharge time)         |
| **Max Continuous Discharge Current** | 180A (\~9 min discharge time)               |
| **Peak Discharge Current**           | 220A (≤ 3s)                                 |

## Table X. QUIVER Propulsion System Configuration

| #   | PART DESCRIPTION                                      | EQ DESIGNATION     | WEIGHT (g) |
| --- | ----------------------------------------------------- | ------------------ | ---------- |
| 1   | Hobbywing XRotor X6 Plus integrated propulsion system | MOTOR,PROP,ESC, LF | 710        |
| 2   | Hobbywing XRotor X6 Plus integrated propulsion system | MOTOR,PROP,ESC, RF | 710        |
| 3   | Hobbywing XRotor X6 Plus integrated propulsion system | MOTOR,PROP,ESC, LR | 710        |
| 4   | Hobbywing XRotor X6 Plus integrated propulsion system | MOTOR,PROP,ESC, RR | 710        |
| 5   | TATTU 14S HV 30000mAh Smart Battery                   | BATTERY, MAIN      | 11250      |

## Table X. Propulsion System Mechanical Interfaces

The Hobbywing XRotor X6 Plus integrated propulsion system must be mounted on a 30 mm diameter tube, with cables routed internally. The system is secured using four included screws.

The battery connects via a specialized Molex connector, featuring a safety latch for secure, simplified installation.

## Electrical Interfaces

- XT60 connector on motor wires
- Specialized Molex connector on battery

## Installation Requirements

Follow manufacturer guidelines for secure mechanical mounting, correct internal cable routing, and proper electrical connections to ensure optimal system performance and safety.

# 7. **Electrical System**

This section provides a comprehensive overview of the electrical design and integration work carried out for the V1 prototype of Project Quiver. It details the planning, layout, and execution of the power and signal systems essential for the first iteration fo Project Quiver, which is engineered to deploy a brush bullet payload. The report outlines power and signal layouts, block diagrams, and wiring schematics, along with an in-depth review of the selected components—from battery systems and power distribution boards to flight controllers and ESCs. Finally, it covers critical considerations such as wiring methods, connector selection, and the integration of control signals via Arduino and Pixhawk interfaces.

### 7.1 System Design and Layout

#### Image X: Power Layout

![image](https://github.com/user-attachments/assets/05333e1d-f8c6-4020-a132-c4570d2996ca)

#### Image X: Signal Layout

![image](https://github.com/user-attachments/assets/7db0d55c-c13d-4540-8c1c-73a995291524)

The electrical power layout is branched off into two sections. One line dedicated to providing HV power to the ESCs via contactor control on the Power PCB. This branch additonally provides power to the PCB for all of the outgoing connections and all internal components. 
The second line is providing HV to the UBEC to give steady and reliable power to the flight controller, telemetry air unit, and additional peripherals. The second line has a physical switch on the positive line before the UBEC to give the user control over power going to the flight controller. 

The signal layout can be thought of mainly two sections, the ESCs to the flight controller and the PCB to the flight controller. These two sections will operate on separate CAN lines. The ESCs will connect to the flight controller's CAN 1 and use the DroneCAN protocol. The battery (currently unused) and the radar altimeter will connect to the CAN2 port. The only additional signal being used will be two aux GPIO signals coming from the pixhawk to the PCB for relay and contactor control 

### 7.2 Hardware Selection 

<details>
<summary><h4>Battery</h4></summary>
<br>
 Tattu 3.5 14S - 53.2V 30000 mAh
  
  ![image](https://github.com/user-attachments/assets/f9de309c-b8de-4f88-8e58-4c6bc1f1584d)

  - Capable of CAN communication. Current battery used is on firmware xx.xx and was not compatible with Ardupilot.
  - Battery side connector: Molex EXTreme 46562-9206 manually latching with 46562-9306 = 46562-2657 (a non-official part number)
  - Mates to: Molex EXTreme 46437-9206 manually latching with 46437-9306
  - See Propulsion System for detailed specs

 Battery Adapter

  ![image](https://github.com/user-attachments/assets/3478ce1d-afa3-4890-ba8c-84ed99c1ae57)

  - Installation notes: Used [6 AWG compression lugs](https://www.mcmaster.com/6926K75/) and 1/4" screw for installation  


</details>

<details>
<summary><h4>Power PCB</h4></summary>
<br>

Summary of capabilities:
- Pre-charge and Contactor control via Arduino MKR QIFI 1010
- 12V power regulation, fused output
- 5V power regulation fused output
- 300A fused output
- PWM, 5V, GND easy access with header pins
- Communication protocols: CAN, UART, RS485, and Aux signals (PWM, GPIO, etc.)
- 24, 14, & 8 position atuomotive connector for easy access to pins
- XT90 input and output connectors 

#### 12V Regulator
[MEAN WELL RSDW40G-12](https://www.mouser.com/ProductDetail/709-RSDW40G-12)

![image](https://github.com/user-attachments/assets/13960d5f-7f96-4037-a489-a25e96aab6e5)

- 40W Rating
- Provides power for on board components and brush bullet dispenser motor
- fused output


#### 5V Regulator
[TRACO Power TMU 3-1211](https://www.mouser.com/ProductDetail/495-TMU3-1211)

- 3W Rating
- Provides power for brush bullet relay and 5V on PWM rails
- fused output 


#### Pre-charge and contactor control 

The [contactor (pg.11) ](https://www.dkxn-wx.com/uploadfile/202406/chongdianzhuangen.pdf) on the PCB controls the HV output going to the ESCs. It is controlled by the user via a toggle switch on their RC that instructs the flight controller to send a signal to the on board Arduino. This allows the user to safely disconnect the power to the ESCs and motor in the case of an emergency or at the end of operation. 
On the PCB, the contactor works in hand with a pre-charge circuit for safe operation. The pre-charge allows the capacitor on the ESCs to be partially filled and prevents a large in rush current once the contactor is closed. This is important to mitigate any electrical arcing and damaging the ESCs. Below is a brief explanation of how the pre-charge and contactor control is handled. 

![image](https://github.com/user-attachments/assets/cd9126dc-1bea-4fef-b471-74b604b15c6c)

- Arduino sends signal to [pre-charge relay (K1) ](https://www.mouser.com/datasheet/2/240/media-3323785.pdf) when it recieves command from flight controller for "contactor close"
  - this allows for a low current to pass through multiple [pre-charge resistors (R1-R3)](https://www.mouser.com/datasheet/2/54/pwr163-777985.pdf), bypassing the contactor, to the ESCs
  - after 5 seconds, the Arduino sends signal to the [contactor relay (K2)](https://www.mouser.com/datasheet/2/240/media-3323426.pdf), effectivly closing the contactor
  - the precharge is then turned off 


#### Arduino
[Arduino MKR WIFI 1010](https://docs.arduino.cc/hardware/mkr-wifi-1010/)

- used to send a timed enable signal for the pre-charge circuit
- after a short period, enable signal sent to close contactor

  <details>
  <summary><h5>Sketch</h5></summary>
  <br>

   [Quiver PT1 sketch.zip](https://github.com/user-attachments/files/19173234/Quiver.PT1.sketch.zip)
      
      ```Arduino
      #include "thingProperties.h"
      #include "WiFiNINA.h"
      #include "utility/wifi_drv.h"
      
      int contactor_pin = 2;
      int precharge_pin = 1;
      int led_green_pin = 26; // Green LED
      int led_red_pin = 25;   // Red LED
      int led_blue_pin = 27;  // Blue LED
      
      int control_input_pin = 16; // Placeholder digital input pin for contactor control
      
      unsigned long lastCloudUpdate = 0;
      const unsigned long cloudUpdateInterval = 2000; // Call ArduinoCloud.update() every 2 seconds
      
      // Debounce variables
      bool lastInputState = false;
      bool lastStableState = false;
      unsigned long debounceTime = 0;
      const unsigned long requiredStableTime = 1000; // 1 second required for stable input
      
      void setup() {
        Serial.begin(9600);
        delay(1500);
        Serial.println("Starting setup...");
      
        initProperties();
      
        // Set initial LED state: green on, red off
        WiFiDrv::pinMode(led_green_pin, OUTPUT);
        WiFiDrv::pinMode(led_red_pin, OUTPUT);
        WiFiDrv::pinMode(led_blue_pin, OUTPUT);
        WiFiDrv::analogWrite(led_green_pin, 255); // Turn on green LED
        WiFiDrv::analogWrite(led_red_pin, 0);    // Turn off red LED
      
        pinMode(contactor_pin, OUTPUT);
        digitalWrite(contactor_pin, LOW);
      
        pinMode(precharge_pin, OUTPUT);
        digitalWrite(precharge_pin, LOW);
      
        pinMode(control_input_pin, INPUT);
      
        connectToWiFiAndCloud();
      }
      
      void loop() {
        unsigned long currentMillis = millis();
      
        // Cloud update handling
        if (WiFi.status() == WL_CONNECTED) {
          if (currentMillis - lastCloudUpdate >= cloudUpdateInterval) {
            lastCloudUpdate = currentMillis;
            ArduinoCloud.update();
          }
        } else {
          Serial.println("WiFi disconnected.");
        }
      
        // Read the control input state and debounce
        bool currentInputState = digitalRead(control_input_pin);
      
        if (currentInputState != lastInputState) {
          // Input state changed, reset the debounce timer
          debounceTime = currentMillis;
          lastInputState = currentInputState;
        }
      
        // Check if the input has been stable for the required time
        if (currentMillis - debounceTime >= requiredStableTime) {
          if (currentInputState != lastStableState) {
            // Update stable state and control the contactor
            lastStableState = currentInputState;
            contactor_control = currentInputState;  // Update contactor control state
            onContactorControlChange();
          }
        }
      }
      
      void connectToWiFiAndCloud() {
        Serial.println("Connecting to WiFi...");
        WiFi.begin(SECRET_SSID, SECRET_OPTIONAL_PASS);
        unsigned long startAttemptTime = millis();
        const unsigned long wifiTimeout = 2000; // 2 seconds timeout
      
        while (WiFi.status() != WL_CONNECTED && millis() - startAttemptTime < wifiTimeout) {
          delay(500);
          Serial.print(".");
        }
      
        if (WiFi.status() == WL_CONNECTED) {
          Serial.println("\nWiFi connected!");
          ArduinoCloud.begin(ArduinoIoTPreferredConnection);
          Serial.println("Connected to Arduino IoT Cloud!");
        } else {
          Serial.println("\nFailed to connect to WiFi within the timeout period.");
        }
      }
      
      void onContactorControlChange() {
        if (contactor_control) {
          // Start precharge when contactor control is enabled
          digitalWrite(precharge_pin, HIGH); // Turn on precharge
          delay(5000); // Wait for 5 seconds to complete precharge
          digitalWrite(contactor_pin, HIGH); // Close the contactor
          delay(500); // Wait for the contactor to close
          digitalWrite(precharge_pin, LOW); // Turn off precharge
      
          // Turn LED red
          WiFiDrv::analogWrite(led_green_pin, 0); // Turn off green LED
          WiFiDrv::analogWrite(led_red_pin, 255); // Turn on red LED
        } 
        else {
          // Turn off both precharge and contactor if contactor control is disabled
          digitalWrite(precharge_pin, LOW);
          digitalWrite(contactor_pin, LOW);
      
          // Turn LED green
          WiFiDrv::analogWrite(led_green_pin, 255); // Turn on green LED
          WiFiDrv::analogWrite(led_red_pin, 0); // Turn off red LED
        }
      }
      
      void onPrechargeControlChange() {
        digitalWrite(precharge_pin, precharge_control ? HIGH : LOW);
      }
      
        
      ```


  </details>

#### Automotive Connectors
- [23 Pos Connector](https://www.mouser.com/ProductDetail/571-1-776087-1)
  - Used for CAN, GPIO signals, and GND to the Pixhawk
- [8 Pos Connector](https://www.mouser.com/ProductDetail/571-1-776280-1)
  - Used for radar altimeter power and CAN needs
- [14 Pos Connector](https://www.mouser.com/ProductDetail/571-1-776267-1)
  - Used for power and signal to Brush Bullet Dispenser

 Detailed pinouts can be found in the TO/FROM table. 

#### Design Files
[CAD and Fab files](https://drive.google.com/drive/folders/1PsYq2oiq2gbZsiwGzrd3abQwZkTmpPvH)
![image](https://github.com/user-attachments/assets/00324fd2-4791-43d9-abb5-c59f96e81a34)

Mouser BOM
| Line | Part Number           | Qty Ordered | Qty Shipped | Backorder | Unit Price | Extended Price | Details                                                                                                                                                                                          |
|------|-----------------------|-------------|-------------|-----------|------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | 504-AMX-300           | 1           | 1           | 0         | 9.310      | 9.31           | SD: F1 / AMX-300; Description: Bussmann / Eaton AMX Fuse, 300 A, 125 / Automotive Fuses; Info: US HTS:8536100040 ECCN:EAR99 COO:CN                                                       |
| 2    | 693-3403.0170.11      | 2           | 2           | 0         | 0.660      | 1.32           | SD: F2 / 3403.0170.11; Description: Schurter UMT 250 2.5A 277V Sl / Surface Mount Fuses; Info: US HTS:8536100040 ECCN:EAR99 COO:CH                                                      |
| 3    | 576-178.6165.0002     | 7           | 7           | 0         | 3.610      | 25.27          | SD: F3, F14, F16, F22 / 178.6165.0002; Description: Littelfuse FLR (ATO) PCB 4-pin / Fuse Holder; Info: US HTS:8536908585 ECCN:EAR99 COO:MX                                                 |
| 4    | 710-7461383           | 2           | 2           | 0         | 2.710      | 5.42           | SD: J1, J2 / 7461383; Description: Wurth Elektronik WP-SHFU Pin-Plate 16 / Terminals; Info: US HTS:8536904000 ECCN:EAR99 COO:DE                                                        |
| 5    | 571-282834-4          | 1           | 1           | 0         | 1.920      | 1.92           | SD: J8 / 282834-4; Description: TE Connectivity 4P SIDE ENTRY 2.54mm / Fixed Terminal Blocks; Info: US HTS:8536694040 ECCN:EAR99 COO:IT                                                   |
| 6    | 200-TSW10625GTRA      | 1           | 1           | 0         | 2.300      | 2.30           | SD: J9 / TSW-106-25-G-T-RA; Description: Samtec Classic PCB Header S / Headers & Wire Housings; Info: US HTS:8536694040 ECCN:EAR99 COO:US                                               |
| 7    | 571-1-776280-1        | 1           | 1           | 0         | 8.520      | 8.52           | SD: J12 / 1-776280-1; Description: TE Connectivity 8 POS RTANG HDR ASSY / Automotive Connectors; Info: US HTS:8536694040 ECCN:EAR99 COO:MX                                               |
| 8    | 200-SSW11401TS        | 2           | 2           | 0         | 1.830      | 3.66           | SD: J14, J15 / SSW-114-01-T-S; Description: Samtec Tiger Buy Socket Str / Headers & Wire Housings; Info: US HTS:8536694040 ECCN:EAR99 COO:VN                                              |
| 9    | 571-1-776087-1        | 1           | 1           | 0         | 11.410     | 11.41          | SD: J17 / 1-776087-1; Description: TE Connectivity / AMP HDR 23POS R/A BLK / Automotive Connectors; Info: US HTS:8536694040 ECCN:EAR99 COO:MX                                            |
| 10   | 571-1-776267-1        | 1           | 1           | 0         | 8.390      | 8.39           | SD: J19 / 1-776267-1; Description: TE Connectivity / AMP 14POS RTANG HDR ASSY / Automotive Connectors; Info: US HTS:8536694040 ECCN:EAR99 COO:US                                           |
| 11   | 849-CPC1718J          | 2           | 2           | 0         | 7.570      | 15.14          | SD: K1 / CPC1718J; Description: IXYS Integrated Circuits DC Only Single Pole / Solid State Relays - PCB Mount; Info: US HTS:8541498000 ECCN:EAR99 COO:PH                                  |
| 12   | 849-CPC1916Y          | 2           | 2           | 0         | 5.870      | 11.74          | SD: K2 / CPC1916Y; Description: IXYS Integrated Circuits 100V Single Pole SIP / Solid State Relays - PCB Mount; Info: US HTS:8541498000 ECCN:EAR99 COO:PH                                 |
| 13   | 720-LST676-Q1R2-1-Z     | 2           | 2           | 0         | 0.300      | 0.60           | SD: LED1 / LS T676-Q1R2-1-Z; Description: ams OSRAM Super Red, 645nm 180 / Standard LEDs - SMD; Info: US HTS:8541410000 ECCN:EAR99 COO:CN                                             |
| 14   | 495-TMU3-1211         | 2           | 2           | 0         | 8.900      | 17.80          | SD: PS1 / TMU 3-1211; Description: TRACO Power 3W 10.8-13.2Vin 5V 6 / Isolated DC/DC Converters - Through Hole; Info: US HTS:8504409580 ECCN:EAR99 COO:TW                           |
| 15   | 522-FMMT555TA         | 2           | 2           | 0         | 0.310      | 0.62           | SD: Q1 / FMMT555TA; Description: Diodes Incorporated PNP High Voltage / Bipolar Transistors - BJT; Info: US HTS:8541210095 ECCN:EAR99 COO:CN                                          |
| 16   | 652-PWR163S-25-50R0F    | 4           | 4           | 0         | 3.940      | 15.76          | SD: R1, R2, R3 / PWR163S-25-50R0F; Description: Bourns 25watts 1% 50 Ohm DP / Thick Film Resistors - SMD; Info: US HTS:8533290000 ECCN:EAR99 COO:CR                                   |
| 17   | 603-RC0805FR-07220RL    | 4           | 4           | 0         | 0.100      | 0.40           | SD: R4, R5 / RC0805FR-07220RL; Description: YAGEO 220 Ohms 125 mW 0805 / Thick Film Resistors - SMD; Info: US HTS:8533210030 ECCN:EAR99 COO:TW                                      |
| 18   | 603-RC0805FR-07100KL    | 4           | 4           | 0         | 0.100      | 0.40           | SD: R6, R9 / RC0805FR-07100KL; Description: YAGEO 100 kOhms 125 mW 080 / Thick Film Resistors - SMD; Info: US HTS:8533210030 ECCN:EAR99 COO:TW                                      |
| 19   | 603-RC0805FR-077K5L     | 4           | 4           | 0         | 0.100      | 0.40           | SD: R7, R11 / RC0805FR-077K5L; Description: YAGEO 7.5 kOhms 125 mW 080 / Thick Film Resistors - SMD; Info: US HTS:8533210030 ECCN:EAR99 COO:TW                                      |
| 20   | 603-RC0603FR-07680RL    | 2           | 2           | 0         | 0.100      | 0.20           | SD: R8 / RC0603FR-07680RL; Description: YAGEO 680 Ohms 100mW 0603 / Thick Film Resistors - SMD; Info: US HTS:8533210030 ECCN:EAR99 COO:TW                                      |
| 21   | 179-SLW-913535-2ASMT    | 2           | 2           | 0         | 0.530      | 1.06           | SD: S1 / SLW-913535-2A-SMT; Description: CUI Devices 9.1 x 3.5 x 3.5 mm, / Slide Switches; Info: US HTS:8536509050 ECCN:EAR99 COO:CN                                          |
| 22   | 782-ABX00023          | 1           | 1           | 0         | 38.600     | 38.60          | SD: G: ARDUINO MKR 1010 / ABX00023; Description: Arduino MKR WIFI 1010 / WiFi Development Tools - 802.11; Info: US HTS:8517620090 ECCN:5A992.C COO:IT                            |
| 23   | 910-TS391LT10         | 1           | 1           | 0         | 28.950     | 28.95          | SD: MFG Part No: TS391LT10; Description: Chip Quik Paste NoClean 35g Sn / Solder; Info: US HTS:8311900000 ECCN:EAR99 COO:CA                                                     |
| 24   | 709-RSDW40G-12        | 1           | 1           | 0         | 46.790     | 46.79          | SD: PS2 / RSDW40G-12; Description: MEAN WELL 18-75Vin 12V 3.333A / Isolated DC/DC Converters - Through Hole; Info: US HTS:8504409580 ECCN:EAR99 COO:TW                       |
| 25   | 710-885012108012      | 4           | 4           | 0         | 1.300      | 5.20           | SD: C1, C2 / 885012108012; Description: Wurth Elektronik WCAP-CSGP 47uF 1206 / Multilayer Ceramic Capacitors MLCC - SMD/SMT; Info: US HTS:8532240020 ECCN:EAR99 COO:TW          |



</details>

<details>
<summary><h4>UBEC</h4></summary>
<br>

![image](https://github.com/user-attachments/assets/b93a61c9-8da2-4238-8c58-437d632dc7aa)

The KDE UBEC "allows for clean, voltage-regulated power for critical flight electronics and peripheral equipment (including 12V aerial photography and high-end UAS equipment)". The UBEC was added to avoid having a secondary power supply to the flight controller and any peripheral systems. The 12V regulator on the PCB would experience too much load if it attempted to power the PCB, brush bullet, and flight controller. Using a UBEC is an easy integration and allows for a clean 12V power delivery to mission critical components. 

A toggle switched was placed on the positive lead going to the UBEC from the battery to give the user manual control over the power flowing through the UBEC to the flight controller. 


</details>

<details>
<summary><h4>XT60 Splitter</h4></summary>
<br>
  
![image](https://github.com/user-attachments/assets/8d76d1ce-e5f8-4611-9f08-0283cbeaf11c)

[TL60-10 Power Distribution Module XT60](https://www.aliexpress.us/item/3256807277265897.html?gatewayAdapt=glo2usa&mp=1&spm=a2g0o.productlist.0.0.69c33d1eTWCvNb)
Nothing too technical here. We opted for a simple splitter to handle all of the XT60 connections to the ESCs. 

</details>

<details>
<summary><h4>ESC</h4></summary>
<br>
  
See Propulsion System section for detailed description on the [HobbyWing X6 Plus](https://www.hobbywing.com/en/products/xrotor-x6-plus269) 

</details>

<details>
<summary><h4>Flight Controller</h4></summary>
<br>

</details>

<details>
<summary><h4>Radar Altimeter</h4></summary>
<br>

[Us-D1 Radar Altimeter](https://ainstein.ai/us-d1-all-weather-radar-altimeter/)

![image](https://github.com/user-attachments/assets/085159ff-bc1a-4e66-8f5e-fc060964ac4c)

The Ainstein AI Altimeter is a small form factor device that reports reliable measurements up to 50m. The US-D1 comes with a Molex (50579204) 4-pin, 2.54mm connector. This connector required a modification in order for us to use it with the 8 position automotive connector. 
 
Verify that the following parameters are used on the Flight Controller:
- CAN_P2_DRIVER = 1 (first can port driver set to driver 1)
- CAN_D2_PROTOCOL = 7 (USD1 protocol for driver 1)
- RNGFND1_TYPE = 33 (USD1_CAN)
- RNGFND1_MIN_CM = 50
- RNGFND1_MAX_CM = 4500
- RNGFND1_GNDCLEAR = 10 or more accurately the distance in centimeters from the range finder to the ground when the vehicle is landed. This value depends on how you have mounted the rangefinder.


It is important to note that the altimeter should not be tested in doors to get accurate readings. Please test the altimeter outside and verify that the distance being read is correct. 


</details>

<details>
<summary><h4>GPS</h4></summary>
<br>

- M9N and M10 GPS from Hollybro
- connects to GPS1 and GPS2 ports on pixhawk

</details>

<details>
<summary><h4>Telemetry</h4></summary>
<br>

[HM30 Air Unit](https://shop.reebot.com/products/mk32-hm30-mk15-air-unit?VariantsId=10820)

![image](https://github.com/user-attachments/assets/be4fdc1a-d2c8-44c8-980a-f5e7c846466b)

- Signal Output: 16 channels of S.BUS, 5 channels of PWM
  
Interface & Ports:
- SBUS: 3-Pin
- Datalink (to FC): UART 4-Pin
- PWM Channel 1 to 5: 6-Pin
- Video Input: Ethernet 8-Pin
- Firmware Upgrade: Type-C

- Dimensions (antenna excluded, fan included): 70 x 55 x 16 mm
- Weight (antenna excluded): 74 g
- Antenna Gain (standard omni): 5 dBi
- Power Input: 11 to 16.8 V (expandable to 4S to 18S with BEC)

[Integration doc](https://docs.google.com/document/d/1c7d-TiKrViZ_PJSGZGZeT6v6mQBDRZmvlZf1WeDICiA/edit?tab=t.0#heading=h.aczyuw2yex2w) prepared by Alexander Dada
</details>

<details>
<summary><h4>Gimbal Camera</h4></summary>
<br>

</details>

<details>
<summary><h4>Brush Bullet Dispenser</h4></summary>
<br>

</details>



### 7.3 Wiring Diagram

![image](https://github.com/user-attachments/assets/6c6033d5-139c-4bda-8aa5-4d28adead154)

#### Table X: TO/FROM Connections

| FROM | Connector | TO | Connector | Cable Length (cm) | AWG | Type | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 12S Tattu Smart Battery | Tattu Adapter  | Power PCB | XT90 |  | 6  | 50V | Location (?) |
| 12S Tattu Smart Battery  | Tattu Adapter | Power PCB | HDR 14POS R/A Pins 7&8 (J19) |  | 20 | CANB | J19 Pin 7 & 8 |
| Power PCB POS Bus A | M5 Ring Terminal | Contactor A | M5 Ring Terminal | custom |  |  |  |
| Contactor B  | M5 Ring Terminal | Power PCB POS Bus B | M5 Ring Terminal  | custom |  |  |  |
| Contactor AUX | loose cables | PowerPCB  | Screw Terminal J8 | custom |  |  | will have to extend cables. Note current layout for wiring |
| Power PCB | HDR 14POS R/A Pins 3,4,5,6 (J19) | Brush Bullet Dispenser Attachment  | 8 pos JST | 40 | 20 | 5V,GND,12V,GND | 3 pins for 12V and GND (2) each, power for relay and motor |
| Power PCB  | PWM Pin 1 (J9) | Brush Bullet Dispenser Attachment | 8 pos JST  | 40 | 24 | Signal | signal for relay  |
| Power PCB  | PWM Pin 2 (J9) | Arduino MKRWiFi 1010 Pin A1 - 16 (J14) | Header or solder |  |  | Signal | Signal from Pixhawk to enable precharge and contactor close  |
| Brush Bullet Dispenser Attachment  | Solder Pad | Brush Bullet Relay (COM) | Screw terminal  |  | 20 | 12V + |  |
| Brush Bullet Relay (NO) | Screw Terminal  | Brush Bullet Motor  | Solder heat shrink  |  | 20 | 12V + |  |
| Bush Bullet Dispenser Attachment  | Solder Pad | Brush Bullet Motor | Solder heat shrink  |  | 20 | 12V GND |  |
| Brush Bullet Dispenser Attachment  | Solder Pad | Brush Bullet Relay (DC+, DC-, IN) | Screw terminal  |  | 20 | 5V, GND, EN |  |
| Power PCB | HDR 23POS R/A Pins 8,11,12 (J17) | Pixhawk CAN 2 | 2mm Molex 4-pin  | 60 | 20 | CANB L, H, GND | will have to use a self solder heat shrink to 24 AWG cable |
| Power PCB | HDR 23POS R/A Pins 1 & 2 (J17) | Pixhawk PWM Main Pin 8 & 7  | Header  | 60 |  | PWM | Send enable signal to  |
| Power PCB | HDR 8POS R/A Pins 6,7,8 (J12) | Radar Altimeter  | Custom |  |  | CAN, 5V | Need to move to CAN B (?)  |
| Power PCB  | XT90 F | TL60-10 | XT90 M (Solder Cables) |  |  |  |  |
| TL60-10 | XT60 | ESC1 | Crimp or XT60 | 83 |  | 50V |  |
| ESC1 | Unsure | Pixhawk CAN | 2mm Molex 4-pin  | 83 + ? | 24 | CAN L, H, GND | I2C Splitter |
| TL60-10 | XT60 | ESC2 | Crimp or XT60 | 83 | 8 | 50V |  |
| ESC2 | Unsure | Pixhawk CAN | 2mm Molex 4-pin  | 83 + ? | 24 | CAN L, H, GND | I2C Splitter |
| TL60-10 | XT60 | ESC3 | Crimp or XT60 | 83 | 8 | 50V |  |
| ESC3 | Unsure | Pixhawk CAN | 2mm Molex 4-pin  | 83 + ? | 24 | CAN L, H, GND | I2C Splitter |
| TL60-10 | XT60 | ESC4 | Crimp or XT60 | 83 | 8 | 50V |  |
| ESC4 | Unsure  | Pixhawk CAN | 2mm Molex 4-pin  | 83 + ? | 24 | CAN L, H, GND | I2C Splitter |
| Tattu Adapter | Spade Terminal  | UBEC Switch | Crimp or XT30 | UBEC Default | 16 | 50V | Positive cable to switch only  |
| UBEC Swtich  | XT30 | UBEC |  |  |  |  |  |
| UBEC | XT30 M | PM02D | XT30 F | Cockpit height | 16 | 12V |  |
| PM02D | XT30 (M or F?) | Pixhawk Power 1 | [2mm Pitch Molex 6-pin](https://www.molex.com/en-us/products/part-detail/5024430670) | Default  | 24 | 5V, I2C |  |
| PM02D | XT30 (M or F?) | HM30 TX | XT30 M |  | 16 | 12V |  |
| HM30 TX | Ethernet | SIYI A8 Gimbal  | 8 Pin Molex |  |  | LAN & PWR |  |

#### Wiring Notes

- Connection from the Power PCB to the attachment interface for the brush bullet dispenser relied on self soldering heatshrink . This was mainly done to allow a conenction from a 20 AWG cable to 24 AWG cable. Some lines were doubled up to account for the higher current needs with a smaller cable. The following cable scheme was used:

  - 12V
    - 3 cables for positive
        -Green, Blue, and Yellow
    - 2 cables for negative
        - Orange and White
  - 5V
    - Red for Positive
    - Black for negative
  - Signal
    - Brown 

- Last minute change to wiring was done by connecting the UBEC directly to the battery adapter. A XXX connector was used with XX AWG cables to connect the UBEC to the same bolts being used for the compression lugs. 
# 8. **Geometry & Structure**

The design of this aircraft centers on accommodating frequent modifications and upgrades, preserving straightforward access to all key components. By employing a modular architecture and standardized interface points, the system can be quickly reconfigured or expanded to integrate novel sensors, payloads, or propulsion elements. Structural integrity is achieved through robust materials such as aluminum 7075 and 3D-printed carbon fiber nylon and connections that distribute loads uniformly. This approach enables the prototype to withstand potentially harsh landings, while finite element analysis (FEA) helps validate each subsystem’s load-bearing capacity. Furthermore, by minimizing mass through efficient structural layouts and selective material use, the aircraft maintains better flight performance, high agility, and reduced power consumption to extend operational times.

---

## 8.1. Overall Geometry

The overall geometry is largely symmetrical, with key components arranged around a central thrust plane. The battery is intentionally placed slightly above this plane, shifting the center of gravity (CG) upward. During mission, lower-mounted attachments help balance the airframe, ensuring that the CG remains near the thrust plane’s center. This symmetrical configuration, combined with the modular design, makes it straightforward to reposition or replace entire subsystems while preserving stable flight characteristics.

Below is a summary of the aircraft’s key dimensional parameters:

| **Parameter**           | **Measurement** |
| ----------------------- | --------------- |
| Folded Width            | 62 cm           |
| Folded Length           | 60 cm           |
| Unfolded Width          | 95 cm           |
| Unfolded Length         | 95 cm           |
| Overall Height          | 68 cm           |
| Max Attachment Height   | 40 cm           |
| Max Attachment Diameter | 30 cm           |

These dimensions ensure balanced weight distribution in both folded and unfolded states while providing adequate space for payloads and accessories.

### Subsystem Weight Breakdown

Below is an approximate weight breakdown for each major subsystem, noting the primary materials involved. These figures are meant to serve as general estimates and may vary based on final manufacturing processes, hardware choices, and tolerances.

| **Subsystem**          | **Material(s)**                           | **Approx. Weight** |
| ---------------------- | ----------------------------------------- | ------------------ |
| Main Chassis           | Aluminum 7075 & Carbon Fiber Nylon        | 1500 g             |
| 4x Motor & Arm         | Carbon Fiber Tubes & Aluminum             | 4200 g             |  
| Landing Gear           | Carbon Fiber & Aluminum                   | 800 g              |   
| Battery Enclosure      | Carbon Fiber Nylon                        | 1100 g             |   
| Electrical Compartment | Carbon Fiber Nylon                        | 200 g              |   
| Avionics               | Aluminum / 3D-Printed CF Nylon            | 300 g              |   
| Camera                 | Camera Lens & Gimbal / Equipment Holder   | 500 g              |   
| Misc. Hardware         | Fasteners, Harness, Electrical Components | 300 g              |   
| **Estimated Total**    | -                                         | **8900 g**         |   

Please note that these weights are not definitive values and should be verified after prototype assembly and testing.

---

## 8.2. Detailed Zones

### Main Chassis

Two parallel aluminum plates—each 3/32" (2.5 mm) thick and fabricated from aluminum 7075—form the central chassis of the aircraft. These plates provide the main structural backbone. They're connected by the motor mounts on the corners and a 3D-printed carbon fiber nylon cube clamped at the center. The center cube accommodates holes on the sides to leave access for the attachment harness.

---

### Motors

Each motor is situated at the end of a 30 cm-long, 30 mm-diameter carbon fiber arm that extends radially from the central chassis. These arms are attached to the plates using hinged, foldable connectors made of aluminum. The hinging mechanism typically includes a locking pin, which secures the arms in flight position and allows rapid folding for compact transport. The motor mounts are supplied by the motor manufacturer, embedded around the motor.

---

### Landing Gear

The landing gear system employs 20 mm-diameter carbon fiber tubes attached with off-the-shelf aluminum housing under the central chassis. Two vertical tubes are connected to one horizontal tube on the bottom with aluminum tube connectors. The tubes position the aircraft at a large ground clearance, giving enough height for any attachments.

---

### Battery Enclosure

Located near the geometric center of the aircraft, the battery enclosure ensures a balanced center of gravity for stable flight control. This enclosure is dimensioned to accommodate the selected battery module, as well as batteries in the same battery family with lower capacity.

**Enclosure Structure:**

- A 3D-printed carbon fiber nylon box that attaches directly to the upper chassis plate. It also provides two sliders for the battery, ensuring that the vertical movement is prevented.
- A 3D-printed carbon fiber nylon hatch on the enclosure, protecting the battery from exterior. A cut-out ensures visibility for the battery on-off button and battery charge indicator.
- A 3D-printed carbon fiber nylon cap over the enclosure, featuring integrated cut-outs for ventilation and weight reduction.

---

### Electrical Compartment

The electrical compartment consolidates the power distribution board (PDB), battery connector, and high-voltage and signal cables between the electrical and propulsion system components. The battery connector is located on a connector stand, which has a latch to lock the battery in place. By placing the electrical compartment between the main chassis plates, the design makes the overall size of the aircraft smaller and simplifies cable routing. The PDB and battery connector are removable for any troubleshooting or replacement.

---

### Avionic Bay

The avionic bay houses core navigation and control components, including flight controllers, GPS antennas, and telemetry antenna. By isolating these critical electronics from power systems, the design maintains cleaner data signals and more accurate sensor readings. The avionics are placed on the top of the battery enclosure.

---

### Belly Equipment

The underside of the aircraft provides a dedicated zone for mounting the attachment, radar altimeter, and the gimbal camera. The attachment is connected to an interface utilizing a quick release mechanism. The interface is connected to the chassis for better structural support. The gimbal camera is located on a 3D-printed holder to increase the view angle. The radar altimeter is placed so that the operational field of view is not affected by the attachment and the landing gear.


### 8.3 FEA analysis

Will demonstrate how the structure will behave under the following forces

- 12 Kg of force acting at each motor (full throttle)

- 12 kg of force acting on the cockpit (weight from all equipment)

- The materials in the study are:
  - Aluminum 6061 for all the foldable motor arm connector, landing gear joints, and motor beam ends.
  - Aluminum 7075 for cockpit plates
  - Carbon fiber for the motor arms and land legs.

**NOTE** Structure is constrained at a “imaginary” plate added in the middle to simulate a solid structure with free movement.

### Displacement
![image](https://github.com/user-attachments/assets/cd100121-ce67-43da-9def-886bd7891a5a)
### Stress 
![image](https://github.com/user-attachments/assets/69b82e52-3998-4c1c-b71e-9e7cb1ae806e)

### Results Summary
- The results yielded a 1.53 safety factor, meaning that the design at full throttle is marginal and could fail if external forces (bad weather, unexpected maneuvers) are acting.

- The max displacement of one of the motor beams reached 10.77 mm

- The max stress occurred at the motor beam to foldable motor arm connector with a value of 17 Mpa.

**Recommendation:** Since these were the results at full throttle, it is unlikely we will be in this condition. The recommendation is to perform a bench test on the motor arm in order to see how it behaves under various throttle outputs.


# 9. **Appendix**

Hey guys how are you doing

