# Reactive Distillation Column Control and Optimization  
![License](https://img.shields.io/badge/license-MIT-blue.svg)

An AI-integrated chemical engineering project focused on the **modeling**, **optimization**, and **control** of reactive distillation (RD) columns using a combination of **first-principles modeling** and **artificial neural networks (ANNs)**.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Project Objectives](#project-objectives)
- [Modeling Methodology](#modeling-methodology)
- [Optimization](#optimization)
- [Control Strategies](#control-strategies)
- [Technologies Used](#technologies-used)
- [Results Summary](#results-summary)
- [Future Scope](#future-scope)
- [Team Members](#team-members)
- [License](#license)

---

## 🔍 Overview

Reactive distillation integrates chemical reaction and separation in a single column, offering benefits like:
- Enhanced conversion for equilibrium-limited reactions
- Reduced energy consumption
- Compact process design

This project explores three stages:
1. **Modeling** the RD column using first-principles and ANN.
2. **Optimizing** operational parameters using surrogate-assisted optimization.
3. **Controlling** the dynamic system using PID and Model Predictive Control (MPC).

---

## 🎯 Project Objectives

- Develop accurate steady-state and dynamic models of the RD column.
- Train ANN surrogate models for real-time prediction.
- Identify optimal process conditions using grid search and ANN.
- Implement control strategies (PID, MPC) to maintain desired performance.

---

## 🧪 Modeling Methodology

### 1. First-Principles Model
Simulates mass and energy balances across the RD column:
- Ideal Vapor-Liquid Equilibrium (VLE)
- Reaction kinetics: A ⇌ B + C
- Simplified tray hydraulics and constant molar overflow

### 2. ANN Surrogate Model
- Inputs: Feed composition, reflux ratio, tray configuration
- Outputs: Product purity, conversion
- Architecture: MLP with ReLU activation, trained on simulation data
- Loss function: Mean Squared Error (MSE)

---

## ⚙️ Optimization

### Goal:
Maximize product purity while minimizing energy use and unreacted feed.

### Decision Variables:
- Reflux ratio  
- Number of reactive trays  
- Feed tray location  
- Feed flow rate  

### Methods Used:
- **Grid Search** using first-principles simulations
- **ANN-assisted optimization** to accelerate evaluation

---

## 🕹️ Control Strategies

### 1. PID Control
- Simple and stable for single-loop systems
- Effective for small disturbances

### 2. Model Predictive Control (MPC)
- Handles multivariable dynamics and constraints
- Stabilizes the system under large disturbances
- Prediction horizon: 10 steps

### 3. Hybrid Approach
- Combine PID for baseline stability
- Use MPC for advanced multivariable control
- Explore ANN-based controllers (e.g., LSTM) for future adaptation

---

## 💻 Technologies Used

- Python  
- Scikit-learn, TensorFlow  
- NumPy, SciPy  
- Matplotlib, Seaborn  
- Aspen Plus (for simulation data)

---

## 📈 Results Summary

| Parameter              | Optimal Value        |
|------------------------|----------------------|
| Reflux Ratio           | ~2.75                |
| Reactive Trays         | 8–9                  |
| Feed Location          | Stage 10             |
| Feed Flow Rate         | ~1.15 mol/min        |
| Product Purity (B)     | >97%                 |
| Conversion of A        | >94%                 |
| ANN Prediction Error   | <2% MAE              |
| MPC Stabilization Time | <3 minutes           |

---

## 🚀 Future Scope

- Implement **real-time MPC** on industrial platforms.
- Train **RNN/LSTM** controllers for predictive control.
- Incorporate **non-ideal thermodynamics** (NRTL/UNIQUAC).
- Use ANN for **closed-loop optimization**.
- Develop **operator training simulators** using dynamic models.

---

## 👥 Team Members

- **Rahul Garg** (B22CH025)  
- **Parth Arora** (B22CH019)  
- **Yogesh Sharma** (B22CH045)  

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
