# 📘 CMOS VLSI Design Workshop (Sky130 + NGSPICE)

A structured hands-on workshop covering **MOSFET fundamentals**, **CMOS inverter design**, and **SPICE simulations** using the **Sky130 PDK**.

---

## 📌 Workshop Overview

This workshop follows a progressive learning path:

- **Day 1:** MOSFET fundamentals and current characteristics  
- **Day 2:** Short-channel effects and CMOS inverter VTC  
- **Day 3:** Switching threshold and transient analysis  
- **Day 4:** Noise margin and robustness  
- **Day 5:** Power supply and device variation  

---

## 🚀 Why This Matters for VLSI

This workshop builds the foundation required for **digital and analog VLSI design**.

### Key Learnings

- **MOSFET Fundamentals**  
  Understanding device operation and current flow regions  

- **CMOS Logic Design**  
  Low-power and efficient digital circuit implementation  

- **CMOS Inverter**  
  The most fundamental building block in digital design  

- **Switching Behavior (VTC)**  
  Input-output relationship and switching threshold  

- **Timing Analysis**  
  Rise/fall delays and circuit speed  

- **Noise Margin**  
  Reliability against disturbances  

- **Power Analysis**  
  Impact of supply voltage scaling  

- **Device Variations**  
  Real-world fabrication effects  

---

# 🧪 Day 1: NMOS Fundamentals

## 📖 Topics Covered

- NMOS structure and operation  
- Threshold voltage (Vt)  
- Regions of operation:
  - Cut-off  
  - Linear (Resistive)  
  - Saturation  

---

## ⚡ Key Equations

### Linear Region
Id ∝ (Vgs - Vt)Vds

### Saturation Region
Id ∝ (Vgs - Vt)^2


---

## 🔬 SPICE Simulation

- Setup SPICE netlist  
- Use **Sky130 models**  
- Sweep:
  - Vgs  
  - Vds  

### Output:
- **Id vs Vds curves**
![spice_code](images/D1_lab_1.png)
![Ngspice_run_d1](images/D1_lab_2.png)
![Ngspice_plot](images/D1_lab_3.png)
![Ngspice_plot_result](images/D1_lab_4.png)



---

# ⚡ Day 2: Short Channel Effects & VTC

## 🔍 Key Concepts

- Long channel → Quadratic behavior  
- Short channel → Linear behavior  

### Velocity Saturation
- Carrier velocity saturates at high electric field  
- Limits drain current  

---

## 🔄 CMOS Inverter Basics

| Input | NMOS | PMOS | Output |
|------|------|------|--------|
| 0    | OFF  | ON   | HIGH   |
| VDD  | ON   | OFF  | LOW    |

---

## 📈 Voltage Transfer Characteristics (VTC)

- Defines switching behavior  
- Identifies operating regions  
![Ngspice_run_d1](images/D2_lab_1.png)
![Ngspice_run_d1](images/D2_lab_2.png)
![Ngspice_run_d1](images/D2_lab_3.png)

---

# 🔁 Day 3: Switching Threshold & Dynamic Analysis

## 📊 VTC Simulation

- Sweep Vin from **0 → VDD**
- Plot Vout vs Vin

---

## 🎯 Switching Threshold (Vm)
Vm = Vin = Vout

- Both NMOS and PMOS are ON  
- Maximum current flows  

---

## ⏱️ Transient Analysis

Measures:

- Rise Delay  
- Fall Delay  

### Design Goal
Vm ≈ VDD / 2
![Ngspice_run_d1](images/D3_lab_1.png)
![Ngspice_run_d1](images/D3_lab_2.png)
![Ngspice_run_d1](images/D3_lab_3.png)
![Ngspice_run_d1](images/D3_lab_4.png)
![Ngspice_run_d1](images/D3_lab_6.png)



---

# 🔐 Day 4: Noise Margin

## 📌 Definition

Noise Margin = Ability to tolerate input noise without incorrect output  

---

## 📏 Parameters

- VOH → Output High  
- VOL → Output Low  
- VIL → Max input LOW  
- VIH → Min input HIGH  
![Ngspice_run_d2](images/D2_theo_1.png)
---

## 📐 Equations
NMH = VOH - VIH
NML = VIL - VOL


---

## ✅ Key Insight

- Larger noise margin → Higher reliability  
- CMOS inverter is inherently robust  

---

# 🔋 Day 5: Power & Device Variations

## ⚡ Power Supply Scaling

### Effects of Lower VDD

**Advantages:**
- Lower power consumption  
- Reduced heat  

**Disadvantages:**
- Increased delay  
- Reduced performance  

---

## 🧬 Device Variations

### Causes

- Variation in **W/L ratio**  
- Oxide thickness variation  

---

### Effects

- Drain current variation  
- VTC shift  
- Switching threshold shift  

---

## 🧪 Observations

- Strong PMOS → Vm shifts right  
- Strong NMOS → Vm shifts left  

---

# 🏁 Final Conclusion

- CMOS inverter is **highly robust**  
- Tolerates:
  - Supply variations  
  - Device variations  

👉 Performance may change, but **logic correctness remains intact**
![Ngspice_run_d1](images/D5_lab_1.png)
![Ngspice_run_d1](images/D5_lab_2.png)
![Ngspice_run_d1](images/D5_lab_3.png)
![Ngspice_run_d1](images/D5_lab_4.png)
![Ngspice_run_d1](images/D5_lab_5.png)

---

## 🛠️ Tools Used

- **NGSPICE**  
- **Sky130 PDK**  
- **VirtualBox / UBUNTU 18.04 LTS Environment**

---
## 🙌 Acknowledgment

This workshop provides a strong foundation for:
- Digital VLSI Design  
- Analog Circuit Design  
- Semiconductor Device Understanding in Static Domain

---
