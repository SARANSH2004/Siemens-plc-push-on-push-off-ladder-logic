# PLC Push ON / Push OFF Control System  
**Siemens PLC | TIA Portal | Ladder Logic**

---

## 📌 Project Overview
This project implements an **industrial Push ON / Push OFF toggle control system** using a **Siemens PLC** and **TIA Portal**.  
A single momentary push button is used to toggle an output device (motor/relay) between ON and OFF states with reliable memory handling and safety logic.

The control logic is designed to meet **industrial automation standards**, ensuring stable operation, noise immunity, and fail-safe behavior.

---

## 🎯 Objectives
- Implement toggle-based push button logic using Ladder Diagram (LD)
- Eliminate false triggering due to button holding or contact bounce
- Ensure output state retention using internal PLC memory
- Validate logic using PLC simulation

---

## 🧰 Tools & Technologies
- Siemens PLC (S7 Series)
- TIA Portal
- Ladder Logic (LD)
- PLCSIM
- Industrial Push Button (NO)
- Relay / Motor Output

---

## ⚙️ Working Logic
1. Push button generates a momentary input signal  
2. Rising-edge detection triggers toggle logic  
3. Internal memory bit stores the ON/OFF state  
4. Output coil is controlled based on memory status  
5. Output toggles state on every valid button press  

---

## 🪜 Ladder Logic Description
- Uses internal memory bit for latching
- Prevents multiple toggles during continuous press
- Ensures clean transition between ON and OFF states
- Default output state is OFF on PLC startup

---

## 📊 I/O Mapping

| Signal Name | Address | Type   | Description |
|------------|--------|--------|-------------|
| Push_Button | I0.0 | Input | Normally Open Push Button |
| Toggle_Memory | M0.0 | Memory | Toggle State Storage |
| Load_Output | Q0.0 | Output | Motor / Relay Control |

---

## 🧪 Simulation & Testing
- Logic tested using Siemens PLCSIM
- Verified toggle behavior for repeated presses
- Confirmed no false triggering during long press
- Output resets safely on PLC restart

---

## 🔐 Safety & Reliability Features
- Input debounce handling
- Interlock logic for stable switching
- Fail-safe OFF state during startup
- Suitable for industrial panel implementation

---

## 🏭 Industrial Applications
- Conveyor belt start/stop control
- Motor ON/OFF switching
- CNC auxiliary equipment control
- Industrial automation panels
- Machine control systems

---

## 📁 Repository Structure
