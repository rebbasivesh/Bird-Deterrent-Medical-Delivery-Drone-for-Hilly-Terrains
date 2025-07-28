# Bird-Deterrent-Medical-Delivery-Drone-for-Hilly-Terrains

#  Proposed Design of a Lightweight Bird Deterrent System for UAV-Based Medical Delivery in Hilly Regions

---

##  Abstract
The use of Unmanned Aerial Vehicles (UAVs) for medical delivery in hilly terrains presents a promising solution for improving access to healthcare. However, mid-flight bird attacks, especially by territorial species, threaten the safety and reliability of such missions. This paper proposes a lightweight and cost-effective bird deterrent system to be integrated into medical drones. The system will combine ultrasonic sound emission, strobe lighting, and reflective elements to effectively deter birds, while maintaining a total weight under 1.5 kg and cost under ₹50,000. The design will also consider environmental challenges such as wind gusts and drizzles. This paper outlines the planned system architecture, component selection, and activation strategy to ensure mission success in adverse conditions.

---

## 🔍 1. Motivation and Need
In remote and hilly regions, traditional transportation of medicines is time-consuming and often delayed due to lack of infrastructure. Drones offer a viable alternative for last-mile medical delivery. However, bird attacks pose a serious operational risk, especially in mid-flight. Preventing such incidents ensures mission success and can be life-saving in time-critical scenarios.

---

## ⚙️ 2. Design Challenges
- Weight and power constraints on drones  
- Operating in unpredictable weather conditions like wind and drizzle  
- Real-time detection and timely deterrence  
- Non-lethal deterrence that does not harm birds  
- Budget limitation of ₹50,000  
- Avoiding false triggers and ensuring robustness

---

## ❓ 3. Problem Statement
A drone delivering medicines in a hilly region faces frequent attacks by birds at approximately 5 km into a 10 km route. The proposed system must:
- Deter bird attacks effectively without harming wildlife
- Function reliably in drizzles and wind gusts
- Add less than 1.5 kg to the drone
- Cost less than ₹50,000
- Consume minimal power

---

## 🧰 4. Proposed System Overview
The deterrent system will consist of:
- **Ultrasonic Speakers** to emit bird-repelling frequencies between 20–30 kHz
- **Strobe Lights** (high-intensity flashing LEDs) to visually distract and scare birds
- **Reflective Tape Panels** mounted on the drone arms for passive deterrence
- **Microcontroller Unit** (e.g., Arduino Nano) to control triggering logic
- **Li-Po Battery Pack** for independent power supply

---

## 🛠️ 5. System Design, Integration and Cost Analysis
The system will be triggered using GPS data at around the 4.8 km mark to pre-empt the attack zone. The electronics will be protected with IP65-rated enclosures and coated PCBs.

### 📋 Estimated Component and Integration Cost:

### Component and Cost Breakdown

| **Component**                  | **Specification**               | **Cost (INR)** |
|-------------------------------|----------------------------------|----------------|
| Drone Frame + Motors          | 1.5kg payload capable            | 20,000         |
| Flight Controller             | Pixhawk / Ardupilot              | 10,000         |
| Ultrasonic Emitter            | 20–40 kHz                        | 3,000          |
| Strobe Light Modules          | High-intensity LEDs              | 1,000          |
| Reflective Panels             | 360° reflective tape             | 500            |
| Battery Pack                  | 4S Li-Po, 5000 mAh               | 5,000          |
| Microcontroller Unit          | ESP32 / STM32                    | 600            |
| Weatherproof Enclosure        | Polycarbonate housing            | 1,000          |
| Misc. (Cables, Frame Mounts)  | Screws, Connectors               | 500            |
| **Total Estimated Cost**      |                                  | **41,600**     |
**Total Estimated Weight**: ~1.35 kg
---

### ✅ **Why Use an Extra Microcontroller Along with Flight Controller?**

1. **Flight Stability Protection**:
   Flight controllers are optimized for handling flight dynamics only. Adding non-flight sensor processing can risk timing issues and destabilize the drone.

2. **Limited I/O & Protocol Support**:
   Flight controllers offer limited GPIO pins and often only support specific peripherals (e.g., GPS, IMU). Extra sensors (ultrasonic, PIR, etc.) need more flexible interfaces.

3. **Avoid Overloading FC CPU**:
   Adding complex logic like bird detection or deterrent control can overload the flight controller’s CPU, affecting real-time flight performance.

4. **Modular Design & Fault Isolation**:
   Separating the deterrence logic into another microcontroller ensures that even if it fails, the drone can still fly safely.

5. **Faster Development & Debugging**:
   Microcontrollers like ESP32 or Arduino are easier to program and debug for sensor interfacing compared to flight controller firmware.

6. **Optional Communication Link**:
   If needed, the external microcontroller can still communicate with the flight controller via UART, I2C, or PWM for synchronized control or data sharing.

---

---

## 🚀 6. Implementation Plan
1. Design Finalization and CAD modeling
2. Procurement of components
3. Hardware assembly and Arduino programming
4. Simulation testing (Gazebo/ROS)
5. Controlled outdoor testing on an RC drone

---

## 📊 7. Comparison with Conventional Drones
- Standard drones lack deterrent systems and are vulnerable to bird strikes
- This drone includes an integrated ultrasonic and visual deterrent system
- Weather-resilient design improves survivability in challenging environments
- Focused mid-flight deterrence ensures energy efficiency
- Custom-built for medical delivery in rural/hilly regions

---

## 🎯 8. Expected Outcomes
- Reliable deterrence against bird attacks
- Operability in light rain and wind
- Easy integration with existing UAV platforms
- Low power consumption due to selective activation
- Modular upgrade capability

---

## 🔮 9. Scope for Future Work
- AI-based bird detection using onboard camera
- Machine learning-based adaptive deterrent logic
- Solar-powered recharge for energy autonomy

---

## 📚 10. References
1. Hussein, M. A., et al., “Bird Deterrence for UAVs: A Review,” IEEE Access, 2021.  
2. R. Sharma, “Design of Ultrasonic Bird Repellent System,” IJSER, 2020.  
3. Zhang et al., “Real-Time Bird Detection for UAVs,” arXiv preprint, 2020.  
4. Blest, A. D., “Eyespots as Anti-predator Mechanisms,” Nature, 2005.  
5. S. Jadhav, “Strobe-Based Bird Repellent,” IJERT, 2020.
