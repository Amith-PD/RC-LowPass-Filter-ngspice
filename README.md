# 📊 RC Low-Pass Filter using ngspice

##  Overview

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

fc​=1/2πRC

---

## 📊 Results

### 🔹 Transient Analysis

* Shows capacitor charging/discharging
* Output lags input

---

### 🔹 AC Analysis

* Flat response at low frequency
* Attenuation after cutoff
* -20 dB/decade slope

results/ac_response and other cases.png 

---

### 🔹 Parameter Variation

| Case | R    | C       | Effect        |
| ---- | ---- | ------- | ------------- |
| 1    | 1kΩ  | 0.1µF   | Higher cutoff |
| 2    | 5kΩ  | 0.047µF | Medium cutoff |
| 3    | 10kΩ | 0.01µF  | Lower cutoff  |


---

## ⚠️ Constraints

* AC source must include `AC 1`
* Frequency range: 10 Hz – 100 kHz
* ngspice does not support `.step`
* Use `.control` block for execution
* Proper file extension `.cir`

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
