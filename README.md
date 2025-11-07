# 🏆 Mechatronic Mastery – Inter-Hostel Robotics Challenge 2025  
### **Submission for Girnar Hostel Tech GC 2025 – Team *GyattArm67***

This repository contains our complete submission for the **Mechatronic Mastery: Inter-Hostel Robotics Challenge 2025**, hosted by the Robotics Club, IIT Delhi.  
The competition evaluates participants across **three progressively challenging tasks**, covering:

✅ Holonomic mobile robot navigation  
✅ Multi-DOF serial manipulator inverse kinematics  
✅ Integrated mobile manipulation (navigation + color‑based pick & place)

Results are not yet released — this repository reflects our **full technical submission**.

---

# 📂 Repository Structure

```
Mechatronic-Mastery/
│
├── Task1A/   → Holonomic Drive Navigation
├── Task2/    → Serial Manipulator Control (IK + trajectories)
├── Task3/    → Integrated Mobile Manipulation
│
├── README.md              ← (You are here)
└── media/ (optional)      ← Videos & presentation (to be added)
```

Each task folder includes:
- CoppeliaSim `.ttt` scene file(s)  
- Lua or Python control scripts  
- Task‑specific README  
- A demonstration video link  

---

# 🧠 Problem Summary  

The challenge involves simulating and controlling both **mobile** and **manipulator** robots inside **CoppeliaSim**.  
The tasks progressively test:

- Holonomic drive kinematics  
- Serial manipulator inverse kinematics  
- Trajectory generation  
- System coordination & sequencing  
- Physically realistic robot motion  

We implemented all logic using **CoppeliaSim + Lua + Python ZMQ Remote API**.

---

# ✅ Task 1A – Holonomic Drive Navigation  
*Arena: HolonomicDrive.ttt*

### 🎯 Objective  
Simulate an omnidirectional mobile robot and autonomously navigate through **five waypoints**, avoiding static obstacles.

### ✅ Features Implemented
- Lua script for base control  
- Three proximity sensors for obstacle detection  
- Smooth linear + rotational velocity control  
- Dynamic, non‑teleporting motion  
- Waypoint switching with distance threshold  
- Sensor‑driven avoidance behavior  

📄 See `Task1A/README.md`

---

# ✅ Task 2 – Serial Manipulator Control  
*Arena: Manipulator.ttt*  
*Robot: UR5 (6‑DOF)*  

### 🎯 Objective  
1. Move end‑effector to provided coordinates (Task 2A).  
2. Execute **circular, square, and sinusoidal** trajectories (Task 2B).

### ✅ Features Implemented
- Full **Inverse Kinematics** control for UR5  
- Python remote API generates joint targets  
- Lua script performs smooth joint motion via `sim.moveToConfig()`  
- Forward Kinematics for debugging & EE verification  
- Safe working envelope, collision‑free execution  

📄 See `Task2/README.md`

---

# ✅ Task 3 – Integrated Mobile Manipulation  
*Arena: MobileManipulator.ttt*  
*Robot: KUKA youBot (5‑DOF arm + 3‑DOF base = 8 DOF)*

### 🎯 Objective  
Navigate, detect cuboid color, pick using IK, and place upright in correct drop zones.

### ✅ Features Implemented
- Keyboard teleoperation for mobile base (Python)  
- Autonomous IK‑based manipulator control (Lua)  
- Signal‑based synchronization:  
  `pickup_now`, `pickup_done`, `drop_now`, `drop_done`  
- Friction‑based gripper (no artificial joints)  
- Stability‑focused placement routine  

📄 See `Task3/README.md`

---

# ▶️ How to Run

### ✅ General
1. Install **CoppeliaSim Educational Edition**  
2. Open the appropriate scene (`.ttt`) for each task  
3. Ensure Lua child scripts are attached  
4. Run Python scripts:  
   ```bash
   python3 <script>.py
   ```  
5. Follow task‑wise instructions inside each folder

---

# 👥 Team  
**Team Name:** *GyattArm67*  
**Hostel:** Girnar Hostel  
**Event:** Girnar Hostel Tech GC 2025 Submission  


---

# ✅ Final Notes  
This repository represents our full submission for the challenge.  
All simulation files, scripts, and documentation have been organized for easy reproduction and evaluation.

