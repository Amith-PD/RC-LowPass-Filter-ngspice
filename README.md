# 📊 RC Low-Pass Filter using ngspice

## 🔷 Overview

This project demonstrates the simulation of an **RC Low-Pass Filter** using ngspice. The circuit is analyzed using **Transient Analysis**, **AC Analysis**, and **Parameter Variation** to study its behavior under different conditions.

---

## 🎯 Objectives

* Analyze time-domain response (Transient)
* Analyze frequency response (AC)
* Determine cutoff frequency
* Study effect of varying R and C

---

## ⚙️ Circuit Description

A simple RC Low-Pass Filter:

* Resistor in series
* Capacitor to ground
* Output taken across capacitor

---

## 🧮 Cutoff Frequency

[
f_c = \frac{1}{2\pi RC}
]

---

## 📁 Project Structure

```
RC-LowPass-Filter-ngspice/
│── README.md
│── circuits/
│     └── rc_lowpass.cir
│── results/
│     ├── transient.png
│     ├── ac_response.png
│     ├── case1.png
│     ├── case2.png
│     └── case3.png
```

---

## ▶️ How to Run

1. Open Command Prompt
2. Navigate to ngspice bin directory:

```
cd /d "D:\VLSI Projects\NGSPICE\Spice64\bin"
```

3. Run simulation:

```
ngspice "path\to\rc_lowpass.cir"
```

---

## 📊 Results

### 🔹 Transient Analysis

* Shows capacitor charging/discharging
* Output lags input

![Transient](results/transient.png)

---

### 🔹 AC Analysis

* Flat response at low frequency
* Attenuation after cutoff
* -20 dB/decade slope

![AC Response](results/ac_response.png)

---

### 🔹 Parameter Variation

| Case | R    | C       | Effect        |
| ---- | ---- | ------- | ------------- |
| 1    | 1kΩ  | 0.1µF   | Higher cutoff |
| 2    | 5kΩ  | 0.047µF | Medium cutoff |
| 3    | 10kΩ | 0.01µF  | Lower cutoff  |

![Case1](results/case1.png)
![Case2](results/case2.png)
![Case3](results/case3.png)

---

## ⚠️ Constraints

* AC source must include `AC 1`
* Frequency range: 10 Hz – 100 kHz
* ngspice does not support `.step`
* Use `.control` block for execution
* Proper file extension `.cir`

---

## ❌ Common Issues

| Problem          | Reason            | Solution         |
| ---------------- | ----------------- | ---------------- |
| Flat graph       | Missing AC source | Add `AC 1`       |
| Command error    | Wrong directory   | Use `/d`         |
| File not running | `.txt` extension  | Rename to `.cir` |

---

## 🚀 Applications

* Signal filtering
* Noise reduction
* Audio systems
* Analog electronics

---

## 📌 Conclusion

The RC Low-Pass Filter behaves as expected:

* Passes low frequencies
* Attenuates high frequencies
* Cutoff depends on R and C values

---

## 🧠 Viva Questions

* What is cutoff frequency?
* Why -20 dB/decade slope?
* Effect of increasing capacitance?
* Difference between AC and transient analysis?

---

## 🛠 Tools Used

* ngspice
* Windows CMD

---

## 👨‍💻 Author

Amit Airodagi
