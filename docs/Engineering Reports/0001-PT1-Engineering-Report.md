# **Project Quiver PT1 Engineering Report**

Chapter assignment: https://docs.google.com/spreadsheets/d/1HtNkbYEaUmdiHmNGzjgIHoH00VwN5BeEsrYEDDL5YV4/edit?gid=0#gid=0

Spearhead Engineering Report: https://docs.google.com/document/d/11yaRfGD6EVfLsOcSKlHVtQumxKxEsTgK/edit

---

# 1. **Introduction**

Hey guys how are you doing

# 2. **Project Requirements**

Hey guys how are you doing

# 3. **Prototype Specifications**

Hey guys how are you doing

# 4. **Mission Performance**

Hey guys how are you doing

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

Hey guys how are you doing

# 8. **Geometry & Structure**

Hey guys how are you doing

# 9. **Appendix**

Hey guys how are you doing

